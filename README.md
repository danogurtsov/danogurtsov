# Dan Ogurtsov

**Web3 special ops** — proven track record in audits and research, hands-on in development too, with solid team-management experience. With an advanced AI toolset.

![Solidity](https://img.shields.io/badge/Solidity-363636?logo=solidity&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![AI / LLMs](https://img.shields.io/badge/AI%20%2F%20LLMs-412991?logo=openai&logoColor=white)

- [X / Twitter](https://x.com/danogurtsov) · [LinkedIn](https://www.linkedin.com/in/danogurtsov/) · [danogurtsov.com](https://danogurtsov.com)

---

- [Audits](#audits)
- [Research](#research)
- [Development](#development)
- [AI & Tooling](#ai--tooling)

## Audits

- **[Pashov Audit Group](https://www.pashov.net/)** — Head of Audits for over 2 years. Built the entire audit-management process from scratch, then optimized and automated it, ending up managing ~500 projects in total.

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

- **Uniswap v4 hook mechanism research** — each repo pairs a working v4 hook with an honest evaluation harness: LP net PnL versus a rebalancing benchmark, the *best-tuned* baselines (not strawmen), rational fee-aware agents, Monte Carlo with confidence intervals, and mainnet fork backtests. The goal is a defensible — sometimes negative — finding, not a marketing claim.
  - **[LVR-minimizing-dynamic-fee-hook](https://github.com/danogurtsov/LVR-minimizing-dynamic-fee-hook)** (2026) — prices the LP fee from realized volatility to fight loss-versus-rebalancing (LVR). Finding: a backward-looking volatility signal lags the move and does not beat a well-tuned static fee — the value is the measurement framework and the open problem it frames.
  - **[inventory-aware-fee-skew-hook](https://github.com/danogurtsov/inventory-aware-fee-skew-hook)** (2026) — an asymmetric fee skewed by the pool's live inventory *state* (discount the rebalancing side, surcharge the worsening one). Finding: a lag-free state signal leans ahead of the directional (Nezlobin) fee on signal quality, but the absolute edge is small and within noise, and a vol-aware fee wins under clustering volatility.

_Coming soon — on-chain anomaly detection, oracles, bridges and protocol analytics._

## Development

- **[noframe-core](https://github.com/danogurtsov/noframe-core)** (2024) — decentralized stablecoin (fixUSD) backed by fixed-yield collateral: CDP engine, oracles, stability pool.
- **[wMORPHO](https://github.com/danogurtsov/wMORPHO)** (2024) — ERC4626 meta-allocator over MetaMorpho vaults, plus a liquid wrapper for the non-transferable MORPHO token.

## AI & Tooling

- **[dandelion](https://github.com/danogurtsov/dandelion)** — reconstructs a protocol's on-chain architecture from addresses, not a repo: resolves code (verified source in any language, or decompiled bytecode), reads real state, and autonomously crawls proxies, roles, reserves and cross-chain deployments into one typed architecture graph. From a single Aave Pool address it maps the whole protocol. Rigorously evaluated: measured membership precision (not just recall), a held-out generalization set, and an ablation that quantifies the LLM's contribution; plus historical block-pinning for incident forensics. The AI sits behind a validation membrane (it proposes, determinism validates, it can only add and never corrupt) with a calibrated precision judge. Model-agnostic reasoning loop, hexagonal, 142 tests + live evals (Python).
- **[deduplicator-merge-advanced](https://github.com/danogurtsov/deduplicator-merge-advanced)** — a Claude-powered fair-merge engine for audit findings: groups overlapping findings by root cause and merges them without losing content or erasing authorship. Ships as an MCP server and a standalone analyzer. LLM-graded evals + offline CI (Python/MCP).
