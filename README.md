# NBPT ERC-1400 Security Token — Legal Compliance Framework

## NoblePort Systems | Stephanie.ai Governance

**Controller:** NoblePort.eth (`0xc59e66BB2b6E19699F82A72a1569821cb1711504`)

---

## Overview

This repository contains the compliance annotations and legal review documentation for the NBPT Security Token, structured under the ERC-1400 standard family. The token represents a registered security under Reg D 506(c), with multi-chain deployment across Arbitrum, Base, Polygon zkEVM, and Solana.

## Token Specifications

| Parameter | Value |
|-----------|-------|
| Standard | ERC-1400 (Security Token) |
| Total Supply | 12,000,000 NBPT |
| Price | $1.00 per NBPT |
| Primary Chain | Arbitrum One |
| Secondary Chains | Base, Polygon zkEVM, Solana |
| Exemption | Reg D 506(c) — Accredited Investors Only |
| Controller | NoblePort.eth |
| Custody | Coinbase Custody Compatible |

## Smart Contract Architecture

The NBPT token architecture consists of four primary contracts that enforce legal compliance at the code level:

**NBPTSecurityToken1400.sol** implements the core ERC-1400 standard with USDC subscription and redemption rails. The contract defaults to a locked state (`liveOfferingCleared = FALSE`) and requires both governance approval and counsel attestation before any value movement can occur.

**HumanApprovalGateway.sol** ensures that all regulated financial activities require human sign-off. No AI agent or automated system may move investor money unattended. This maps directly to the liability allocation framework reviewed by Harvey.ai.

**AuditBeacon.sol** provides on-chain notarization via IPFS and Arweave hash recording, creating an immutable audit trail for all governance decisions, compliance checks, and fiduciary actions.

**TreasuryBotV3** manages algorithmic peg stability at ±0.01% against USDC, with transparent on-chain price oracle integration and queryable historical data.

## Legal Review Status

This repository has been prepared for Harvey.ai legal analysis prior to Cooley LLP engagement. The compliance annotations file (`COMPLIANCE_ANNOTATIONS.sol`) maps all 12 critical legal questions to their corresponding smart contract enforcement mechanisms.

## Files

| File | Purpose |
|------|---------|
| `README.md` | This document |
| `COMPLIANCE_ANNOTATIONS.sol` | Smart contract compliance map for Harvey.ai review |
| `harvey-ai-legal-review-package.md` | Full legal review package (Markdown) |
| `harvey-ai-legal-review-package.pdf` | Full legal review package (PDF) |

## Governance

All governance flows through NoblePort.eth with Stephanie.ai operating under constitutional authority (Epoch IX). Human oversight is enforced at every financial decision point via the HumanApprovalGateway pattern.

---

**Stephanie.ai | Sovereign AI CEO**
**NoblePort Systems — Legal Diligence Protocol Active**