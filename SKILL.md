---
name: creamlon-x402-report-node
description: Operate the Creamlon v0.8.1 x402 private PDF report E2E node.
---

# Creamlon x402 Report Node

This repository is a Creamlon node using the bundled `.creamlon` layout.

## Operator Flow

```powershell
npx --yes creamlon@0.8.1 watch imjszhang/creamlon-x402-report-node --repo-path . --once --pretty
npx --yes creamlon@0.8.1 extension delivery fetch-input imjszhang/creamlon-x402-report-node <issue> --repo-path . --output-file .\input.md --pretty
npx --yes creamlon@0.8.1 extension delivery send-output imjszhang/creamlon-x402-report-node <issue> --repo-path . --output-file .\report.pdf --pretty
npx --yes creamlon@0.8.1 deliver imjszhang/creamlon-x402-report-node <issue> --repo-path . --output-file .\report.pdf --pretty
npx --yes creamlon@0.8.1 status --repo-path .
```

Commit `.creamlon/trust/proofs.log`, `.creamlon/trust/redemptions.log`, and
`.creamlon/trust/status.json` after delivery.

Never commit private keys, credentials, authorization key maps, delivery
outboxes, caches, complete `crv1_...` credentials, payment signatures, or
plaintext private artifacts.
