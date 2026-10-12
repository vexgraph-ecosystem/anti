# anti — R6 creative superapp

Future builds belong to [b](https://github.com/vex-graph/b). No runnable game
target exists yet.

## Current State

**Draft — unfinished, not finalized.** Every contract below is a design goal.

**Role:** R6 superapp — composes IDE, DAW, drawing and game/creative workflows
over R1–R5 public contracts. These are future workflows, not implemented products.
R2 storage/computation, R3 drivers, R4 interfaces and R5 applications retain their
own implementations and independent lifetimes under the host.

**Implemented and proven:** nothing. Repository documentation and license only; no `src/`,
no engine code and no test partition.

**Platforms proven:** none.

## What it is
`anti` is a superapp blueprint, able to compose several creative applications
and shared workflows. Its game/world-editor ambition remains one possible
workflow, not the entirety of its scope or a shipped engine.

## Depends on (Vertical Integration Law allowlist)
Borrows public shapes and registered workflows from R1–R5 to build;
owns no OS/window/memory management itself. Standalone-capable or
Kernel-registered.

## Scope and Limitations

**Scope (intended):** R6 creative workflow composition: IDE, DAW, drawing and
game tooling, supervised through the host and public lower-tier contracts.

**Deliberately not covered:** no OS/window/memory management (borrowed from
R1–R5); GPU shaders/dispatch remain Graphvex R3; no lower-tier implementation is owned
here.

**Known limits and gaps:** these are design goals, not a shipped superapp. R2
is split between Vexspoke CPU computation/behavior and Relational Engine
memory/storage/native C search; migration is staged with the retained Vexspoke
ABI/default allocator. No C/Rust atomic-layout equivalence, automatic schema
migration or implemented app integration is implied. See the ecosystem readiness
Gist for granular scope and gaps.

## Layout
- Engine (future): `src/` — editor, world, physics, scripting seams.
- Tests (future): add a `tests/anti/` partition in the shared `../../tests` repo (mirrored per
  unit, the Test Tree Mirror Law); no test file lives inside this repo's source
  directories (the Test Segregation Law).

## Laws that govern work here
- Constitution: the [canonical preferences.md Gist](https://gist.github.com/vex-graph/4132a6c45cb6d3797c3e8eff2e94035a); real, Git-ignored `../../gist/PREFERENCES.md`, not a Vexspoke file or symlink. Lower tiers never include R6 headers or code.
- Commits land in THIS repo root, one cohesive unit each; never push unless asked.
- One public class per `.h`/`.c` pair, `(*ptr).field` (never `->`), dest-last
  params, `-Wall -Wextra -Werror`.
