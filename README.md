# Zena

**Blockchain Protocol Engineer — payments & settlement · smart contracts · zero-knowledge · L2**

Six years shipping production protocols end-to-end at Tokamak Network (Ethereum L2):
token-economy contracts, a live staking protocol maintained through external audits,
zkVM applications, and privacy-preserving settlement systems.
Now building open-source infrastructure for stablecoin payments.

📍 Seoul · UTC+9 · open to remote protocol / smart-contract roles

---

## Now building — stablecoin payment rails

| | What | Status |
|---|---|---|
| [**token-kit**](https://github.com/Zena-park/token-kit) | Modular ERC-20 issuance kit following Circle's FiatToken: byte-identical EIP-3009 type hashes (x402 clients work unchanged), timelock + Guardian veto on issuance authority and upgrades | Apache-2.0 · 103 Foundry tests incl. symbolic (Halmos) |
| [**x402-kit**](https://github.com/Zena-park/x402-kit) | [x402](https://www.x402.org) payments for HTTP APIs: one-line seller middleware, capped buyer `fetch` wrapper, self-hostable facilitator. Any EIP-3009 token directly, any ERC-20 via Permit2; EOA / ERC-1271 / ERC-6492 signers; open-amount (`upto`) payments | Apache-2.0 · TypeScript · 203 unit tests + on-chain e2e · [on npm](https://www.npmjs.com/org/x402.kit) as `@x402.kit/*` |

Design notes I care about in this work: issuance authority that can be vetoed, spending
caps enforced by construction on the payer side, spec-exact wire compatibility, and
tests that pin EIP-712 digests to golden vectors so a refactor can't silently change
what users sign.

## Zero-knowledge & privacy (2026)

| Project | What it is |
|---|---|
| [**zkScatter**](https://github.com/Zena-park/scatter-dex) | Privacy-preserving settlement protocol — private OTC trading and bulk payouts on one ZK stack: Groth16 commitment pools, gasless relayed claims, compliant identity gating |
| [**zk-X509**](https://github.com/Zena-park/zk-X509) | On-chain identity from existing X.509 certificates (Korean NPKI, eID, corporate CAs) via SP1 zkVM — only nullifiers on-chain, private keys never enter the zkVM. MIT · live on Sepolia → [zk-x509.web.app](https://zk-x509.web.app) |
| **zk-card-wallet** 🔒 | X.509-authenticated hardware wallet: JavaCard applet (secure channel, dual secp256k1 / BabyJubJub signing) + circom proving pipeline + mobile app |
| [**ethrex**](https://github.com/tokamak-network/ethrex) | SP1 zkVM proving integrated into a Rust L2 client — bridge guest program, proving profiling baseline |

## Protocol & infrastructure (2020–2026)

- [**TON Staking V2**](https://github.com/tokamak-network/ton-staking-v2) — live seigniorage & staking protocol; founded the repo, top contributor, maintained three years through external audits
- [**TONStarter**](https://github.com/tokamak-network/tonstarter-contracts) — IDO launchpad in production (2021–22): sale / staking / reward contracts, vesting vault factory
- [**Rollup metadata registry**](https://github.com/tokamak-network/tokamak-rollup-metadata-repository) + [checker](https://github.com/tokamak-network/tokamak-rollup-metadata-checker) — L2 registration standard used across the ecosystem
- [**DAO governance stack**](https://github.com/tokamak-network/dao-community-version) — original DAO contracts / backend (2020) and the 2025 community rebuild
- [**ChainForge Studio**](https://github.com/Zena-park/chainforge) — modular app-chain (rollup) factory on ethrex: web wizard → deployable rollup spec + L1 contract deployment
- [**Tokamon Go**](https://github.com/Zena-park/tokamon) — location-based TON reward service: contracts + web + iOS + listener · live at [tokamon.io](https://tokamon.io)
- Full Uniswap V3 stack fork and integration on an optimistic rollup (contracts, smart order router, interface, analytics)

## How I work

- **AI-agent development pipeline, verification first.** I design the decomposition,
  specs, and acceptance checks; coding agents implement; every PR passes layered AI
  reviewers (Claude · Copilot · CodeRabbit · Sonar) with mandatory feedback-resolution
  commits before merge. Tool claims get re-measured, not trusted.
- **Throughput this enables:** ~5,600 commits / 1,000+ merged PRs in H1 2026 as a single
  engineer, across the repos above. Lifetime in one ecosystem: 9,000+ commits, 1,748
  merged PRs (94.6% merge rate).
- **Verification stack:** Foundry + Halmos symbolic tests, EIP-712 golden vectors,
  Slither in CI, on-chain e2e harnesses.

## Stack

`Solidity` `Foundry / Halmos` `TypeScript` `Rust` `Java (JavaCard)` `SP1 zkVM` `Groth16 / circom`
`EIP-712 · EIP-3009 · Permit2 · ERC-1271 / 6492` `Uniswap V3/V4` `OP-stack` `Node.js` `Docker` `GCP / AWS`

## Also

- Lecturer, Korea University — smart contract development (blockchain course)
- 🔒 = private repository; contribution metrics verifiable on request
