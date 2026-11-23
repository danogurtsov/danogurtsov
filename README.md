# Dan Ogurtsov

**Web3 special ops** - on-chain mechanics, smart contracts and on-chain data, leading strong technical teams.

![Solidity](https://img.shields.io/badge/Solidity-363636?logo=solidity&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![AI / LLMs](https://img.shields.io/badge/AI%20%2F%20LLMs-412991?logo=openai&logoColor=white)

[X / Twitter](https://x.com/danogurtsov) · [LinkedIn](https://www.linkedin.com/in/danogurtsov/) · [danogurtsov.com](https://danogurtsov.com)

- **2024 - 2026** — Head of Audits, [Pashov Audit Group](https://www.pashov.com/)
- **2022 - 2024** — Senior Research Engineer, [MixBytes](https://mixbytes.io/)
- **2021 - 2022** — DeFi Research Lead, [P2P.org](https://p2p.org)
- **2020 - 2021** — Solo Independent Solidity Auditor

Founded: [Odd Sequence](https://oddsequence.com)

---

- [Development](#development)
- [AI & Tooling](#ai--tooling)
- [Audits](#audits)
- [Research](#research)

## Development

- **[tremolo-contracts](https://github.com/danogurtsov/tremolo-contracts)**, **[tremolo-web](https://github.com/danogurtsov/tremolo-web)** (2026) — an on-chain market for realized volatility: a dApp with Solidity contracts on testnet, backed by real research and thoroughly tested, plus a React/Next.js web app with wallet integration — **[live](https://app.tremolo.markets/)**.
- **[noframe-core](https://github.com/danogurtsov/noframe-core)** (2024) — decentralized stablecoin (fixUSD) backed by fixed-yield collateral: CDP engine, oracles, stability pool.
- **[wMORPHO](https://github.com/danogurtsov/wMORPHO)** (2024) — ERC4626 meta-allocator over MetaMorpho vaults, plus a liquid wrapper for the non-transferable MORPHO token.

## AI & Tooling

- **[pentimento](https://github.com/danogurtsov/pentimento)** — an AI-orchestrated audit pipeline: deterministic signals route the search, an adversarial protocol verifies each finding and computes its verdict in code, and every confirmed finding gets a real, executed proof-of-concept — never just a model's claim. (Python)
- **[dandelion](https://github.com/danogurtsov/dandelion)** — reconstructs a protocol's on-chain architecture from addresses alone, no repo needed: resolves code, reads real state, and crawls proxies, roles, reserves and cross-chain deployments into one typed graph. Rigorously evaluated: membership precision (not just recall), a held-out generalization set, an LLM ablation. The AI proposes, determinism validates — it can only add, never corrupt. 142 tests + live evals (Python).
- **[deduplicator-merge-advanced](https://github.com/danogurtsov/deduplicator-merge-advanced)** — a Claude-powered fair-merge engine for audit findings: groups overlapping findings by root cause and merges them without losing content or erasing authorship. Ships as an MCP server and a standalone analyzer. LLM-graded evals + offline CI (Python/MCP).

## Audits

- **[Pashov Audit Group](https://www.pashov.com/)** — Head of Audits for over 2 years. Built the entire audit-management process from scratch, then optimized and automated it, ending up managing ~500 projects in total.

  <details>
  <summary>Recommendation from <a href="https://x.com/pashov"><strong>Pashov</strong></a> on <a href="https://www.linkedin.com/in/danogurtsov/">LinkedIn</a></summary>

  > Dan was Head of Audits at Pashov Audit Group for over 2 years, leading every audit end to end. He led ~500 security engagements, at one point handling 25 audits in a single month with double-digit clients running in parallel, and he kept all of it on track through countless issues and fires. On top of that he built tons of internal tools and processes we still rely on every day. Dan is highly skilled, sharp under pressure, and just as strong with people and process as he is with technology. Any team would be lucky to have him.

  </details>

- **[audits](https://github.com/danogurtsov/audits)** — personal list of every audit I was myself an auditor on with a public report available (starting with early Code4rena contests in 2022, then Mixbytes audits, then Pashov Audit Group audits).

## Research

- **[P2P.org](https://p2p.org)** — DeFi Research Lead.

  <details>
  <summary>Recommendation from <a href="https://www.linkedin.com/in/grigoryvasilkov/"><strong>Grigory Vasilkov</strong></a>, CISO at Lido & P2P.org, on <a href="https://www.linkedin.com/in/danogurtsov/">LinkedIn</a></summary>

  > Dan led the DeFi research team under my supervision. He trained the team on smart-contracts and EVM, built processes, documentation and reporting. Dan is proficient in complex DeFi mechanics, complicated smart-contract systems, analysis of complex transactions, DeFi projects vulnerabilities, Solidity development and transaction testing in fork networks. He has perfect communication within the team and arranges a culture of professional judgment.

  </details>

- **[LVR-minimizing-dynamic-fee-hook](https://github.com/danogurtsov/LVR-minimizing-dynamic-fee-hook)** (2026) — prices the LP fee from realized volatility to fight LVR. Finding: the backward-looking signal lags and loses to a well-tuned static fee — the value is the measurement framework.
- **[inventory-aware-fee-skew-hook](https://github.com/danogurtsov/inventory-aware-fee-skew-hook)** (2026) — an asymmetric fee skewed by the pool's live inventory state. Finding: a lag-free signal edges out the directional (Nezlobin) fee, but the gain is small and within noise, and loses under clustering volatility.
- **[Reducing False Positives](https://www.oddsequence.com/research/reducing-false-positives.pdf)** (academic PDF) — a survey of 100 sources across 10 approaches to reducing false positives in security tooling: hybrid SAST+LLM pipelines eliminate 94-98% of them, and proof-of-concept validation reaches zero by actually confirming the bug is real, not just pattern-matching.
