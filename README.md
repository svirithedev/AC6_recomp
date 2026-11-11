# AC6 technical reference

A reference-only fork of [sal063/AC6_recomp](https://github.com/sal063/AC6_recomp), retaining AC6-specific reverse-engineering findings for reading.

The tracked material contains annotated host patches and an address map. The original AC6 gameplay routines were generated locally from the retail executable and are not present in upstream Git. This fork does not recover their missing bodies or provide a complete aircraft, missile or enemy-AI implementation.

## Read these files

| File | What it contains |
|---|---|
| [Flight dynamics](reference/flight/ac6_fps_physics_fix.cpp) | The complete upstream annotated flight-timing patch, preserved byte for byte. Its comments identify force/input/update routines, aircraft fields, energy loss, path-direction behavior and ground-state transitions. |
| [Input context](reference/input/input_context.cpp.txt) | Selected native input-layout and context observations, excluding most Windows keyboard/mouse injection machinery. |
| [Frame timing](reference/timing/frame_delta.cpp.txt) | The upstream observation about quantized frame deltas and unlocked-rate bias. |
| [Function map](reference/functions.tsv) | 10,527 address-keyed entries extracted from the upstream configuration; 10,492 generic address labels and 35 unnamed entries. These are not recovered semantic function names. |
| [Provenance](SOURCE_PROVENANCE.md) | Exact upstream commit, original paths, excerpt spans, transformations and source hashes. |

The flight file remains an archived **host patch**: its imports, hook macros and calls refer to the removed SDK and untracked generated routines. They are retained to preserve the original analysis, not as a compilable program. Excerpts likewise are reading material, not complete translation units. Claims of verification or measurement inside those files belong to the upstream authors; this fork has not independently reproduced them.

## Removed

The current tree excludes the vendored SDK, compiler/code-generator integration, CMake and presets, launcher/build scripts, port application and entry points, renderer/backends, asset extraction/export tools and original build/modding documentation. No executable, game ISO, XEX, game asset or generated retail-game routine is included. There is no build or launch workflow.

Normal upstream Git history remains available through the fork relationship. The current default branch is the reference-only snapshot.

## How to use it

Use the preserved annotations to form research questions and identify candidate routines. Compare their reported behavior with reproducible gameplay measurements before relying on it. Exact addresses concern the upstream executable revision, advertised as the US release; another region/revision must be identified separately.

For an independently written game, pass descriptive findings and acceptance scenarios to implementation work. This reference is not a ready gameplay library, and translating retail routines into another language would not establish rights to reuse them.

## License

[BSD-3-Clause](LICENSE), with the upstream notice preserved. The license covers contributions for which the licensors hold rights; it does not grant rights to publisher-owned game files. No game data was used to prepare this fork.
