# anti — R5 3D game engine

**Role:** R5 Interactable — 5-column editor, bindless rendering, meshlets,
physics, `darkbase` persistence. The `anti` name lives here (per the Identity
& Naming Transition Law: the engine core moved to `vexspoke`, the game engine
kept the name).
**Status:** stub (LICENSE only; no engine code yet).

## What it is
`anti` is the end-user 3D game engine of the ecosystem: world editing,
meshlet pipelines on `graphvex`, scene UI on `darling-framework`, storage on
`darkbase` — supervised as an R1 `Application` by the `hotcwap` Kernel.

## Depends on (Vertical Integration Law allowlist)
Borrows shapes from R1–R4 (arenas, windows, GPU, UI, connectors) to build;
owns no OS/window/memory management itself. Standalone-capable or
Kernel-registered.

## Layout
- Engine (future): `src/` — editor, world, physics, scripting seams.
- Tests: umbrella `tests/` has no `anti/` partition yet; until then keep seam
  tests in-repo under `tests/` (never inside source dirs, per the Test
  Segregation Law).

## Laws that govern work here
- Constitution: `../../preferences.md` (umbrella symlink → `ecosystem/vexspoke/preferences.md`).
- Commits land in THIS repo root, one cohesive unit each; never push unless asked.
- One public class per `.h`/`.c` pair, `(*ptr).field` (never `->`), dest-last
  params, `-Wall -Wextra -Werror`.
