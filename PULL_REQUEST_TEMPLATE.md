<!-- What does this change, and why? Link the issue it fixes. -->

## Checks

- [ ] Tests and lint pass locally (core: `gofmt -l .`, `go vet ./...`, `go test ./...`; Action and dashboard: `npm run lint` where present, `npm test`, `npm run build`)
- [ ] User-facing change (flags, inputs, outputs, exit codes, schema, what the dashboard shows): a matching [BudgetGate/docs](https://github.com/BudgetGate/docs) PR is linked
- [ ] Measurement change: before and after numbers from a contract on testnet are in this description
- [ ] Action `src/` change: `dist/` rebuilt and committed

## What you ran

<!-- The commands and what they printed. Say what you did not check. -->
