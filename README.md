# Dr. Fraudsworth's Finance Factory

A tax-driven Decentralized Finance (DeFi) protocol on the Solana blockchain, featuring dynamic epochs, autonomous carnage events, and real-yield SOL rewards for stakers.

Dr. Fraudsworth's Finance Factory is a mainnet-deployed protocol centered on a closed economic loop. Unlike traditional inflationary tokenomics, this system utilizes a novel mechanism where trading taxes are autonomously allocated to supply reduction and staker rewards.

---

## Technical Evolution: From Prototyping to Mainnet

Prior to the full protocol deployment, a rigorous testing phase was conducted to evaluate various liquidity architectures and automated market maker (AMM) models.

### Protocol Prototyping
* **PARODY Asset:** An mock asset to be deployed from sol wallet `GNZ14A8rTsLMCSUcna44Li9bCkfurfe7nbFmr8UpSnZc`.
* **The Pivot from Pump.fun:** The initial deployment utilized a standard pump.fun AMM. However, testing determined that the static nature of standard bonding curves was insufficient for the protocol's tax-recycling requirements.
* **Migration to Meteora:** To resolve these limitations, the protocol migrated to **Meteora**, leveraging its **Dynamic Fee** architecture. This transition allowed for optimized liquidity capture and real-time fee adjustment, establishing the foundation for the current Finance Factory infrastructure.

---

## Core Economic Mechanisms

The protocol implements a circular economy where trading activity generates tangible value for participants:

### 1. Automated Tax Distribution
Every swap executed through the AMM incurs a configurable tax (ranging from 1% to 14% based on the current Epoch). 
* **71% to PROFIT Stakers:** Distributed as real SOL yield.
* **24% to Carnage Fund:** Reserved for autonomous market buy-back operations.
* **5% to Treasury:** Designated for protocol maintenance and ecosystem growth.

### 2. VRF-Driven Epoch State Machine
The protocol’s temporal cycles are governed by **Switchboard VRF** (Verifiable Random Function). This ensures that epoch transitions, tax rate adjustments, and carnage event triggers are cryptographically random and resistant to administrative manipulation.

### 3. Carnage Events
Upon a VRF-triggered Carnage event, the accumulated Carnage Fund executes autonomous buy-and-burn operations. This process permanently reduces the circulating supply, theoretically increasing the scarcity of the remaining tokens.

---

## Deployed Programs (Solana Mainnet)

| Program | Address | Status |
| :--- | :--- | :--- |
| **AMM** | `5JsSAL3kJDUWD4ZveYXYZmgm1eVqueesTZVdAvtZg8cR` | OtterSec Verified |
| **Transfer Hook** | `CiQPQrmQh6BPhb9k7dFnsEs5gKPgdrvNKFc5xie5xVGd` | OtterSec Verified |
| **Tax Program** | `43fZGRtmEsP7ExnJE1dbTbNjaP1ncvVmMPusSeksWGEj` | OtterSec Verified |
| **Epoch Program** | `4Heqc8QEjJCspHR8y96wgZBnBfbe3Qb8N6JBZMQt9iw2` | OtterSec Verified |
| **Staking** | `12b3t1cNiAUoYLiWFEnFa4w6qYxVAiqCWU7KZuzLPYtH` | OtterSec Verified |
| **Conversion Vault** | `5uawA6ehYTu69Ggvm3LSK84qFawPKxbWgfngwj15NRJ` | OtterSec Verified |

---

## Security and Governance

* **Institutional-Grade Audits:** The protocol underwent three AI-assisted security reviews—SOS, Bulwark, and BOK Formal Verification—analyzing over 130 potential findings across on-chain and off-chain layers.
* **Multisig Governance:** All program upgrade authorities are secured by a **2-of-3 Squads v4 multisig** with enforced timelocks.
* **Verifiable Randomness:** The integration of Switchboard VRF ensures that all outcomes are on-chain and verifiable, removing human bias from the protocol's mechanics.

---

## Repository Structure

The project was developed across 104 documented phases, providing full transparency into the architectural decision-making process.

```text
programs/           -- Core Anchor programs (AMM, Tax, Epoch, Staking, Vault)
app/                -- Next.js 16 Production Frontend
docs-site/          -- Nextra Protocol Documentation
.planning/          -- Comprehensive 104-phase development history
.audit/             -- Security audit reports and remediation logs
