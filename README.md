# anti — R5 3D game engine

## CLion: CMake is IDE metadata only

Open this repository root as a CMake project. `CMakeLists.txt` is an IDE-only
blueprint entry: there are no production sources or C23 source targets yet,
so there is nothing to provide semantic diagnostics or inlay hints for.
No fake declarations, dependency downloads, linking or application runner are
wired into it. IDE appearance is user-verified.

Future builds belong to [b](https://github.com/vex-graph/b). No runnable game
target or standalone runtime build is claimed by this metadata entry.

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
- Tests: the shared `tests/` repo hosts a `tests/anti/` partition (mirrored per
  unit, the Test Tree Mirror Law); no test file lives inside this repo's source
  directories (the Test Segregation Law).

## Laws that govern work here
- Constitution: the universal [`preferences.md`](../../ecosystem/vexspoke/preferences.md) (canonical file; the workspace root links to it).
- Commits land in THIS repo root, one cohesive unit each; never push unless asked.
- One public class per `.h`/`.c` pair, `(*ptr).field` (never `->`), dest-last
  params, `-Wall -Wextra -Werror`.
