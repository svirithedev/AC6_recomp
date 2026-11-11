# Source provenance

Prepared 12 November 2026 from [sal063/AC6_recomp](https://github.com/sal063/AC6_recomp).

Upstream commit: `09144bb092ad871584808aeead69c395edbd5200` (22 August 2026).

This is a reference-only derivative of the public repository, not a decompilation of an ISO supplied by the user. No upstream program or extraction script was executed.

| Retained file | Upstream source | Treatment |
|---|---|---|
| `LICENSE` | `LICENSE` | Byte-for-byte copy; all notice and license terms retained. |
| `reference/flight/ac6_fps_physics_fix.cpp` | `src/ac6_backend_fixes/ac6_fps_physics_fix.cpp` | Byte-for-byte complete file; archived host patch, including its original annotations and wrapper context. |
| `reference/input/input_context.cpp.txt` | `src/ac6_backend_fixes/ac6_kbm_input.cpp` | Original lines 3-18, 106-128, 147-154 and 1400-1408; only added provenance/section comments. |
| `reference/timing/frame_delta.cpp.txt` | `src/render_hooks.cpp` | Original lines 211-218; only added provenance/section comments. |
| `reference/functions.tsv` | `ac6recomp_config.toml`, `[functions]` | Exported address and name fields to a tab-separated lookup; added label-status classification. Build/codegen configuration and runtime patch directives are not retained. |
| `README.md`, `.gitignore`, this file | Newly authored | Describe the actual retained scope and prevent accidental addition of local game files. |

## Original blob SHA-256 checksums

- `LICENSE`: `f8c7147eba0225be836dd7f701bd9e254b76386271fe0a57955ee479864b1c97`
- `ac6recomp_config.toml`: `5c82a1798a2a48d1c91aca7e627572c0540573828d35bba2e2f0dda39618ed8a`
- `src/ac6_backend_fixes/ac6_fps_physics_fix.cpp`: `0dadb2a66681f77145e521c78721c294d10b891312fcd39d38a10ff3d0eab3f7`
- `src/ac6_backend_fixes/ac6_kbm_input.cpp`: `fedb7ea1a5c658704508628e343ed77fc217bf9f09bba3c06adbd2a961fb537b`
- `src/render_hooks.cpp`: `1e8d1db080ea87bb62edfbb4885e9b64541d6d21c0276b84412bbec2372101e5`

## Limits

The address map identifies translation entries, not gameplay semantics. Its names are generic or absent. Underlying original game bodies, missile guidance, enemy AI and decoded aircraft tuning tables are not in this retained source set. Upstream patch comments sometimes reference research documents not tracked by the source repository; those documents are not available here.

All other upstream tracked paths are absent from the reference-only tree. The fork retains Git ancestry; removing build files from the current tree is not purging the upstream history.
