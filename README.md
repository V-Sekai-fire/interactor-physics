# interactor-physics

The physics interactor: a text command in and reply bytes out, over a vendored rigid-body physics engine scene.

## What it is for

It answers the interactor contract for physics, and replies with positions and velocities as integer micrometres so a reply compares against the entity packet with no float codec in between. It is meant to run as a sandboxed riscv64 guest. Only the interactor contract builds from this repository; the engine and its wiring are sources without a build.

## Build and run

```sh
cmake -S thirdparty/interactor -B build
cmake --build build
ctest --test-dir build
```

## Licence

MIT; see `LICENSE`. Files with an Apache-2.0 SPDX header, and the vendored engine, are Apache-2.0.
