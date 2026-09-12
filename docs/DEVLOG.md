# Nightmare Creatures development log

## 2026-09-03 — canonical Track 01 identity

The release audit found a merged 26-track BIN identity in the prepared source.
A read-only prefix hash of the owned merged BIN produced the exact canonical
Track 01 size, MD5, SHA-1, and CRC32. The SHA-1 matched the earlier portfolio
audit.

The source now keeps the merged identity as a compatibility entry and adds the
canonical Track 01 identity. `disc_probe.json` and `catalog_identity.json` now
name `Nightmare Creatures (USA).cue` and
`Nightmare Creatures (USA) (Track 01).bin`. No retail data was copied.

Consulted leads:

- `_runs/knowledge/reviews/2026-09-02-public-disc-identity-audit.md`
- `https://openretro.org/game/c4768fa3-1b87-454a-90c2-acd9ead92166/edit`

The web source was used only to confirm canonical filenames. The owned
read-only hashes remain the identity evidence. No package or publication gate
has passed yet.

## 2026-09-04 v0.1.2 POSIX setup-copy candidate

This candidate pins PSXRecomp 40ce47896026be52bcaae7de03b69766e0bd03e4 and recomp-ui be8ac1d03ee19d55394b5a5f2d9d1506edd56659.
Linux and macOS packages use native CMake, Ninja, Python, C, and C++ tools.
Windows keeps the portable toolchain route. This change does not change game
code or the graduation state. Build-only CI and every exact-package release
gate must pass before publication.

## 2026-09-13 - Reconcile published source into main

The default branch now includes the published v0.1.2 source. The release workflow uses the existing PSX-PUB-031 indentation repair. Later catalog identities and the current recomp-ui repository URL are preserved. The pinned runtime and UI commits match v0.1.2. No new package, release, gameplay test, or source-pin promotion is claimed.

Corpus consulted: PSX-PUB-031 and FAIL-142. The existing audit_release_workflow.py parser and regression supply the repair. Primary reference: https://github.com/softprops/action-gh-release documents overwrite_files under with. Source checks cover YAML structure, Actionlint, title executable-name tests when present, manifest versions, and exact release gitlinks.
