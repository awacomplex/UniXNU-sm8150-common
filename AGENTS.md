# AGENTS.md — UniXNU-sm8150-common

- Scope: shared SM8150 hardware description and platform code only.
- Board-specific values (memory span, reserved regions, wiring, power policy,
  display, partitions) belong to the device repository.
- Every hardware value must name its source: kernel DTSI path, device node, or
  measured log. Unverified values stay as TODO.
- Keep `patches/xnu/series` ordered and review every patch against SM8150; do not
  copy T733-specific patches.
