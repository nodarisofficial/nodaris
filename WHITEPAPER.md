# Nodaris (NDRS) — Whitepaper (Draft v0.1)

## 1. Overview

Nodaris (ticker: **NDRS**) is a decentralized, peer-to-peer digital currency built as a fork of Bitcoin Core, using a CPU/phone-friendly proof-of-work algorithm (Yespower) instead of SHA-256. The goal is to let ordinary people mine using phones and laptops, not just specialized ASIC hardware.

This document is a draft. Numbers and dates will be finalized before public launch.

## 2. Key Parameters

| Parameter | Value |
|---|---|
| Name | Nodaris |
| Ticker | NDRS |
| Consensus | Proof-of-Work (Yespower, N=2048, r=8) |
| Max supply | 19,000,000 NDRS (hard-capped in consensus code) |
| Block time | 2 minutes (target) |
| Block reward (initial) | 10 NDRS |
| Halving interval | 950,000 blocks (~3.6 years) |
| Difficulty adjustment | LWMA (per-block retarget) |
| Address prefix | `ndrs1...` (bech32), base58 prefixes unique to Nodaris |
| Estimated final coin mined | ~108 years after launch |

## 3. Supply Schedule

Nodaris follows a Bitcoin-style diminishing issuance:

- Year 0–3.6: 10 NDRS/block
- Year 3.6–7.2: 5 NDRS/block
- Year 7.2–10.8: 2.5 NDRS/block
- ...continuing to halve every ~3.6 years until the 19,000,000 cap is asymptotically reached (~108 years)

The maximum supply is enforced by the consensus rules of every full node. No entity — including the founder — can increase it without a hard fork that requires the agreement of the entire network. There is no admin key, no mint function, and no mechanism to create coins outside of mining rewards.

## 4. Fair Launch

Nodaris launches the way Bitcoin did: with no premine and no reserved allocation.

- No coins exist before the genesis block. No code path allocates coins to any address outside of normal block rewards.
- The launch date and exact start time are announced in advance. Software and instructions are published for everyone at the same time.
- The founder mines under the same rules, with the same software and the same difficulty as every other participant, starting at the same moment.
- Anyone with more hardware will mine more blocks, as with any proof-of-work coin. There is no special access for the founder.
- All blocks and addresses are public, so anyone can verify the distribution using the blockchain and a block explorer.

## 5. Mining

Nodaris uses Yespower, a memory-hard proof-of-work function designed to run efficiently on ordinary CPUs (phones, laptops) while resisting ASIC/GPU dominance. This is a deliberate design choice to keep mining accessible.

Getting started (early phase): run a Nodaris full node (`nodarisd`) and a CPU miner that requests block templates via RPC (`getblocktemplate`) and submits solved blocks (`submitblock`). Mining pool software and a simplified miner app are planned for a later phase.

## 6. Network

- Genesis block message: "Nodaris 19/Sep/2026 Fair launch no premine mined by the people" (test genesis; final message/timestamp will be re-mined at public launch)
- Seed nodes: to be published at launch (initial testing via community-run and cloud-hosted nodes)
- P2P port: 19333 (mainnet)
- RPC port: 19332 (mainnet)

## 7. Roadmap

1. Internal testing (completed): genesis mined, PoW verified, multi-node sync tested, difficulty retargeting (LWMA) verified
2. Community testnet with early testers
3. Public mainnet launch at an announced time: final genesis, software and mining guide released to everyone at once
4. Block explorer and basic wallet application
5. Mining pool software
6. Listing on smaller/decentralized exchanges as adoption grows

## 8. Risks & Disclaimers

- Nodaris is an experimental cryptocurrency. It has no guaranteed value, and nothing in this document should be read as investment advice or a promise of returns.
- Cryptocurrency regulations vary by country and may change. Users are responsible for complying with their local laws, including tax obligations.
- As with Bitcoin, lost private keys mean permanently lost coins — there is no recovery mechanism.
- This software has not been professionally audited. Use at your own risk, particularly during the early testnet/mainnet phases.

## 9. Contact & Community

_To be added: website, GitHub repository, Telegram/X links._

---

*This is a living document and will be updated as the project develops. Version 0.1 — draft.*
