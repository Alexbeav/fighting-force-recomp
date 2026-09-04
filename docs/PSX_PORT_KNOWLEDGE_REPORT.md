# Fighting Force port knowledge report

## Identity and lane

- Supported revision: USA `SLUS-00433`
- Architecture: PSXRecomp static recompilation with interpreter fallback
- License boundary: project files use `GPL-3.0-only`; framework and game data
  keep separate rights and licenses
- Source provenance gap: the legacy Wave 1 package has no
  `project-manifest.toml` or `docs/FEASIBILITY.md`

## Current result

The clean RetComM scaffold, pinned emitter build, retail-disc generation,
retail-BIOS generation, Release runtime build, and a 25-second headless startup
gate passed. The route reached 6049 frames with no fatal state or automatic
freeze dump.

The current result is distribution preparation only. It does not establish a
portfolio quality state. Operator-visible gameplay, input, audio, saves, and
package-install checks remain open.

## Corpus consulted

Before work, the run checked the portfolio sweep, findings registry, finding
candidates, failure catalog, regression ledger, source pin, and distribution
playbook. The CRLF Bash failure and absolute-path scaffold leak matched the
existing RetComM Studio review. The missing Ninja error was an environment
selection issue. The accepted portable toolchain fixed it without a framework
source change.

## Next decisive test

Build the setup-host archive from the clean source commit. Install that exact
archive in a fresh path that contains spaces. Then ask Alex to test visible
gameplay from the installed package.

## Publication update — 2026-09-03

The next standalone package candidate is `v0.1.1` for Windows x64, Linux
x64, macOS ARM64, and macOS x64. It uses package-only framework child
`e081d29da2fa9862204f63e6b2004d76f1d0cb2d`. Build-only CI and native package gates remain open. This
does not change the title's quality claim.

## 2026-09-04 v0.1.2 POSIX setup-copy candidate

This candidate pins PSXRecomp 40ce47896026be52bcaae7de03b69766e0bd03e4 and recomp-ui be8ac1d03ee19d55394b5a5f2d9d1506edd56659.
Linux and macOS packages use native CMake, Ninja, Python, C, and C++ tools.
Windows keeps the portable toolchain route. This change does not change game
code or the graduation state. Build-only CI and every exact-package release
gate must pass before publication.
