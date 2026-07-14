# Aethersailor compatibility patch

This repository tracks SubBoost v2.6.0 and keeps all SubBoost features intact.

Runtime compatibility changes:

- If a filtered testable group has matching nodes, the generated group contains
  those nodes; if no member matches, it contains `DIRECT`.
- Custom rule providers preserve their source format. MRS sources use an `.mrs`
  cache, YAML sources use `.yaml`, and text/list sources use `.txt`. This avoids
  feeding YAML rule files to Mihomo's MRS decoder.

The image is built by GitHub Actions and published to GHCR.
