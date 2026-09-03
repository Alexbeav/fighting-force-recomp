# Fighting Force validation receipt

## Scope

- Game: Fighting Force, USA, `SLUS-00433`
- Version: `0.1.0`
- Catalog ID: `fighting-force-psx`
- Release repository: `Alexbeav/fighting-force-recomp`
- Publication state: not published

## Frozen inputs

- The source disc identity is in `catalog_identity.json`.
- The required BIOS is a legal SCPH-1001 dump. The package does not support
  OpenBIOS.
- `framework_pins.txt` and the submodule gitlinks record the framework inputs.
- Generated retail code, the game executable, the disc, and the BIOS remain
  outside Git.

## Local build evidence

The portable `cmake-clang-v1` 1.0.14 toolchain built both emitters. Generation
accepted the recorded 27-track disc identity and the retail BIOS. CMake then
built `Fighting_Force__Recompiled.exe` in Release mode.

The hidden, launcher-free, software-renderer boot ran for 25 seconds. The
bounded gate stopped the active process. Its final heartbeat recorded:

- Frame count: `6049`
- VBlank raises: `6049`
- Fatal state: none
- Automatic freeze dumps: `0`
- Failed freeze dumps: `0`

This result proves a headless startup route. It does not prove visible gameplay,
audio, input, saves, or full-game correctness.

## Open release gates

1. Build and audit the setup-host archive from a clean source revision.
2. Install the exact archive in a clean path that contains spaces.
3. Run the exact installed package through the required operator gameplay test.
4. Redownload and audit every private draft archive.
5. Bind publication approval to the exact version and manifest.

The title must not be public while any gate is open.
