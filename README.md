# LatteDrop

A personal macOS music visualizer in the spirit of MilkDrop, built around one goal: visuals that land exactly on the beat, even through AirPods.

**Status:** specification stage, no code yet · **License:** MIT · **Русская версия:** [README.ru.md](README.ru.md)

## The idea

- Reacts to sound from **any app** on the Mac via a Core Audio process tap; renders with Metal.
- **Beat-accurate:** it predicts the next beat instead of reacting late, and compensates the output latency of the current device (built-in speakers, wired, AirPods).
- Handles both ends of music: strict 4/4 electronic and free-rhythm ambient, classical or jazz, and decides on its own which one is playing.
- Three render subsystems cover the looks: a classic MilkDrop-style feedback raster, a vector/oscilloscope renderer, and compute particles.
- Presets are JSON files with hot reload.

Scope is deliberately narrow: macOS 26 on Apple Silicon only, a normal window, no distribution, no `.milk` import, no ML.

## Plan

The full specification is [docs/SPEC.md](docs/SPEC.md) (in Russian, v2.0). Work goes in stages W0–W6; the first is W0: process tap → RMS → a coloured rectangle that follows the sound. A `beatbench` tool measures beat timing error against acceptance thresholds before any visuals get polished.

---

Built by [Semyon Morgunov](https://s.morgunov.tech) with Claude Code as pair programmer.
