# 11O-007: Circup clear-cache and README help

Contribution record for [Adafruit Circup](https://github.com/adafruit/circup). This work addressed [issue #221](https://github.com/adafruit/circup/issues/221) and [issue #170](https://github.com/adafruit/circup/issues/170).

**Status:** [PR #292](https://github.com/adafruit/circup/pull/292) merged on 16 November 2026. The Build CI / test check passed on PR head [41bd6c1](https://github.com/adafruit/circup/commit/41bd6c1748e9254224e15b32482690bcb2a2e722). The merge commit is [9dbb3c0](https://github.com/adafruit/circup/commit/9dbb3c017d88f75ce87072c7c7f3e45bf27f99ba).

## Problems

Issue #221 requests a command to remove Circup's saved state after problems such as a broken bundle download. Issue #170 reports that the README's CLI help output had fallen behind the current commands and options.

## Changes

- Adds the boardless <code>circup clear-cache</code> command. It asks for confirmation before deleting Circup's data directory, which contains downloaded bundles and local bundle settings, and reports when there is nothing to clear.
- Refreshes the README's complete <code>circup --help</code> example and adds a test that checks the documented output against the Click command.

## Validation

See [validation.md](validation.md) for local and CI results. The upstream change is preserved in [patches/circup-clear-cache.patch](patches/circup-clear-cache.patch).
