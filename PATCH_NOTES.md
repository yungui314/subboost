# Aethersailor compatibility patch

This repository tracks SubBoost v2.6.0 and keeps all SubBoost features intact.

The only runtime behavior change is in proxy-group generation: if a filtered
testable group has matching nodes, the generated group contains those nodes;
if no member matches, the generated group contains `DIRECT`. This mirrors the
empty-group fallback used by Aethersailor/SubConverter-Extended and prevents
invalid empty Clash/Mihomo groups without introducing proxy-group cycles.

The image is built by GitHub Actions and published to GHCR.
