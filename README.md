# creamlon-x402-report-node

Creamlon v0.8.1 E2E node for a paid private PDF report flow.

This repository intentionally uses the bundled node layout:

- `.creamlon/manifest.yaml` is the public Creamlon manifest.
- `.creamlon/trust/` contains public proof and redemption records.
- private keys, credential stores, delivery state, and outboxes remain local.

The node sells one-time credentials for `x402-analysis-report` through x402
payment hints, then receives markdown briefs and returns PDF reports through
HPKE private delivery.
