<p align="center"><img src="avatar.png" width="120" alt="Budget Gate logo: a resource-cost gauge behind a gate bar"></p>

# Budget Gate

**Catch Soroban resource-cost regressions in pull requests.**

Budget Gate simulates your contract's calls through the Soroban RPC (`simulateTransaction`), records CPU instructions, read and write bytes, and footprint entries as a baseline, and flags a pull request when a function costs more than it did or gets close to the network's per-transaction limits, which it reads live from the network.

It gates pull requests on cost measured for each function on a real network, which estimators, rent calculators and static analyzers do not set out to do, and it complements them.

**Demo:** [75 seconds, with captions](https://budgetgate.github.io/docs/#see-it-run).

## Repositories

- **[soroban-budget-core](https://github.com/BudgetGate/soroban-budget-core)**: the Go CLI that measures and compares. Latest release: [v0.2.3](https://github.com/BudgetGate/soroban-budget-core/releases/tag/v0.2.3).
- **[soroban-budget-action](https://github.com/BudgetGate/soroban-budget-action)**: the GitHub Action that runs core on pull requests and keeps one report comment up to date. Latest release: [v0.2.2](https://github.com/BudgetGate/soroban-budget-action/releases/tag/v0.2.2).
- **[soroban-budget-dashboard](https://github.com/BudgetGate/soroban-budget-dashboard)**: charts a contract's cost history over commits ([live](https://budgetgate-dashboard.vercel.app/)).
- **[docs](https://github.com/BudgetGate/docs)**: user documentation at [budgetgate.github.io/docs](https://budgetgate.github.io/docs/).

## Status

Early-stage. Not audited and not production-ready. Measuring changed contracts is verified on Stellar testnet; on mainnet, only a read-only call has been measured.
