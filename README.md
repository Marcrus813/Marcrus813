<div align="center">

# Marcus

### Web3 Wallet & Backend Engineer

Self-driven software engineer with 5 years of professional experience, specializing in Web3 and wallet development. Strong understanding of blockchain technologies, transaction flows, wallet architecture, and digital-asset security, with a passion for building secure and reliable wallet solutions. Experienced in adapting quickly to evolving technologies and solving complex problems under pressure while balancing security, performance, and product requirements. DeFi is a strong area of interest, complemented by a broader passion for the Web3 ecosystem. Clear communicator who works effectively in collaborative, fast-paced environments and continuously seeks to learn and improve.

[![Email](https://img.shields.io/badge/Email-yuchengsong813%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:yuchengsong813@gmail.com)

</div>

---

## 💼 What I Do

- Design and build multi-chain wallet and custody systems (Bitcoin, Ethereum, Solana, TRON)
- Develop MPC/TSS threshold-signature infrastructure and distributed signing services
- Own deposit / withdrawal / consolidation / hot-to-cold / cold-to-hot pipelines and chain sync (scanner) modules
- Build wallet management, reconciliation, balance-sheet, and financial-settlement platforms
- Design cross-chain bridges, Layer 2 PoS economics, and Layer 1 LSP integration
- Build order-matching engines and market-maker systems for event prediction markets

---

## 🛠️ Tech Stack

**Languages**

![Solidity](https://img.shields.io/badge/Solidity-363636?style=for-the-badge&logo=solidity&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

**Chains**

![Bitcoin](https://img.shields.io/badge/Bitcoin-F7931A?style=for-the-badge&logo=bitcoin&logoColor=white)
![Ethereum](https://img.shields.io/badge/Ethereum-3C3C3D?style=for-the-badge&logo=ethereum&logoColor=white)
![Solana](https://img.shields.io/badge/Solana-9945FF?style=for-the-badge&logo=solana&logoColor=white)
![TRON](https://img.shields.io/badge/TRON-EF0027?style=for-the-badge&logo=tron&logoColor=white)

**Data & Infrastructure**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

**Smart Contracts**

![Hardhat](https://img.shields.io/badge/Hardhat-FFF100?style=for-the-badge&logo=hardhat&logoColor=black)
![Foundry](https://img.shields.io/badge/Foundry-000000?style=for-the-badge&logo=ethereum&logoColor=white)
![OpenZeppelin](https://img.shields.io/badge/OpenZeppelin-4E5EE4?style=for-the-badge&logo=openzeppelin&logoColor=white)

---

## 🧠 Skills

- Proficient in programming languages such as Solidity, Go, C#, JavaScript, and TypeScript
- Proficient in relational databases such as PostgreSQL, MySQL, Oracle, and MSSQL
- Proficient in non-relational databases such as Redis, MongoDB, and LevelDB
- Skilled in using Linux and Docker for routine maintenance
- Familiar with concepts related to hash functions, digital signature algorithms, and threshold signature schemes
- Familiar with the operating mechanism of Bitcoin
- Familiar with the operating mechanism of Ethereum, as well as the EVM mechanism and its features
- Familiar with the operating mechanism of Solana
- In-depth understanding of the underlying logic and source code of mainstream DeFi protocols such as Uniswap V2, Uniswap V3, and Aave V3
- Familiar with the implementation of LSP products; has participated in and led the design and development of LSP projects
- Familiar with the basic concepts, implementation mechanisms, and source code of EigenLayer, and has experience in secondary development based on EigenLayer
- Familiar with the development logic of multi-chain cryptocurrency wallets

---

## 🚀 Featured Projects

### CEX Wallet System

**2021.09 - 2022.12**

A multi-tenant, multi-chain wallet system for a centralized exchange (CEX) that unifies the address, transaction, and signing models of heterogeneous chains such as Bitcoin, Ethereum, Solana, and TRON, providing core fund-flow capabilities including deposits, withdrawals, consolidation, and hot-cold transfers.

- Led the overall architecture as wallet architect: built a unified multi-chain gateway (gRPC + adapter pattern) behind a single interface for address conversion/validation, block and transaction queries, fee estimation, transaction construction, and broadcasting, so onboarding a new chain only requires implementing and registering the interface with zero upstream changes.
- Designed and developed the offline signing machine: managed private keys with KMS and wrapped ECDSA / EdDSA / Schnorr multi-algorithm signing.
- Owned the full deposit / withdrawal / consolidation / hot-to-cold / cold-to-hot pipeline: designed the withdrawal order state machine, decoupled signing from broadcasting with a persistent queue, and guaranteed in-order outbound transactions per address using a nonce watermark table with on-chain calibration.
- Built the chain sync (scanner) module: designed per-chain scanning strategies, and used platform-address Bloom filtering plus streamed in-memory processing to persist only relevant transactions.

**Tech Stack:** Solidity, Go, gRPC, KMS, ECDSA / EdDSA / Schnorr

---

### CEX Wallet Management & Reconciliation System

**2023.01 - 2023.10**

A wallet management and reconciliation system for CEX wallet operations - an operational and financial middle platform outside the wallet core that gives finance, risk, and operations staff a unified data view and operation entry point, covering configuration management, fund flows, transaction reconciliation, balance sheet, and financial settlement.

- Designed and implemented a role-based access control system covering users, roles, menus, and departments, granting differentiated data views and permissions to finance, operations, risk, and marketing roles.
- Managed asset and cold-wallet address configuration: parameterized token decimals, minimum consolidation amount, cold-transfer trigger amount, and hot-wallet balance alert threshold, maintaining addresses and balances across multiple chains and assets.
- Managed user wallets and deposit/withdrawal flows: chained deposits, withdrawals, consolidation, hot-to-cold, cold-to-hot, and manual crediting into an end-to-end flow, paired with large-withdrawal approval and automated review.
- Built the reconciliation and reporting system: generated daily/weekly/monthly/quarterly/annual reports by chain, asset, and transaction category, and reconciled trade count, amount, and fee consumption against business-layer deposit/withdrawal data.
- Designed the balance-sheet and settlement modules: implemented borrowing/repayment, balance-sheet snapshots, and statements, using the accounting logic "total assets = account balance + total withdrawals + hot-to-cold; total liabilities = total deposits + settlement + cold-to-hot" to keep funds balanced.
- Built a data dashboard surfacing total deposits, total withdrawals, active address count, total assets, total liabilities, settled amounts, total borrowings, and total repayments.

**Tech Stack:** Go, RBAC, Reconciliation, Financial Settlement

---

### Cross-chain Staking Project

**2023.11 - 2024.10**

Layer 2 infrastructure whose security derives from Layer 1: it uses PoS to secure the Layer 2 network and bridges tokens to a Layer 1 LSP protocol to leverage staked tokens. Users earn yield from both Layer 2 PoS and the Layer 1 LSP, and can earn additional yield through restaking protocols such as EigenLayer by staking stTokens from the LSP.

- Developed the Layer 2 PoS module, implementing the PoS economic model so users can stake/unstake as Stakers or participate in consensus as Operators, with the Layer 2 consensus layer rewarding and penalizing Operators.
- Developed the cross-chain bridge module, bridging Stakers' Layer 2 tokens to Layer 1 for LSP staking.
- Developed the Layer 1 LSP module, receiving Layer 2 tokens and integrating with a mining pool to launch Validators and earn Layer 1 consensus rewards.

**Tech Stack:** Go, Cross-chain Bridges, PoS Economics, LSP, EigenLayer

---

### MPC Asset Management System

**2024.11 - 2025.12**

A multi-party asset management system based on threshold signature schemes (TSS): the full private key is never generated at any point, and one key system covers multiple chains including Bitcoin, EVM-compatible chains (ECDSA), and Solana (EdDSA).

- Technology selection and algorithm research: used TSS as the protocol engine and wrapped it into a deployable, networked, reusable distributed node runtime supporting GG18 ECDSA and Ed25519 threshold-signature Keygen / Signing / Resharing, laying the foundation for security, stability, and reliability.
- Designed the Manager + multi TSS Node architecture: the Manager acts as the coordination layer, exposing an HTTP API, managing node liveness, running the pre-signing ask step and task dispatch, and verifying the final signature with the CPK - holding no key shares itself; the actual multi-party computation runs between Nodes, each storing only its local share, with every inter-node message double-signed and membership-checked.
- Built key-share storage and disaster recovery: supported three tiers (local file / AWS Secrets Manager / Shamir + KMS + S3), and in production re-split each node's share via "shares of shares" with envelope encryption and dispersed storage, achieving both loss prevention and leak prevention.
- Implemented the signing flow and fault tolerance: an ask-authorized → sign two-phase signing flow, uninterrupted signing when nodes within threshold go offline, CPK verification and digest caching to prevent duplicate signing, and a Blame mechanism to attribute bad shares so failures are explainable and traceable.

**Tech Stack:** Go, MPC/TSS, GG18 ECDSA, Ed25519, AWS KMS, Shamir

---

### Event Prediction Market

**2025.12 - 2026.08**

A decentralized event prediction market with built-in market maker support, enabling flexible market-making strategies.

- Designed and developed the market maker module, supporting flexible strategies across the full event lifecycle (pre-market → mid-session → end-game): a layered market-making pipeline of "initialization → order/quote/inventory/spread sync → volatility and depth metrics → passive pricing → active risk adjustment → unified cancel/repost execution" producing key inputs such as reserve price, dynamic spread, and target depth; the active layer supports multiple risk modes and manual intervention, and converges end-game risk via time decay as settlement approaches.
- Designed and developed the admin console, managing and monitoring event lifecycle, user trades, market maker onboarding, event settlement, asset management, and risk control.
- Developed the order matching engine for multi-outcome prediction markets (Yes/No, Up/Down), implementing direct matching and cross-book complementary matching (implied liquidity at 1 - price) on an in-memory price-time priority order book, with support for limit / budget market orders, decimal precision control, Redis quote sync, and atomic settlement, improving liquidity and matching efficiency.

**Tech Stack:** Go, Order Matching Engine, Market Maker, Redis

---

## 📊 GitHub Activity

<div align="center">

<img src="https://ghchart.rshah.org/Marcrus813" alt="GitHub Contribution Chart" />

</div>

---

## 🎓 Education

**University of Liverpool** — Bachelor's Degree, Information and Computing Science (2017 - 2021)

---

## 💬 Get in Touch

I'm always open to discussing wallet architecture, digital-asset security, MPC/TSS, and DeFi protocols.

**Email:** [yuchengsong813@gmail.com](mailto:yuchengsong813@gmail.com)

---

<div align="center">

_Building secure, reliable Web3 infrastructure, one wallet at a time_ 🔐

</div>
