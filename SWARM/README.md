# SWARM

A low-poly voxel **FPS horde-survival** game that runs entirely in the browser — one self-contained `index.html`, no build step, no asset files. Survive endless waves of an alien swarm across three rotating environments, beat bosses to unlock new weapons, and chase a high score.

**▶ Play it: https://nikolai-paquin.github.io/Swarm/**

![SWARM](screenshot.png)

## Features

- **Full 3D FPS** — WASD + mouse-look, sprint, jump, and real verticality (ramps, mesas, jump-up cover) that both you and the enemies navigate.
- **Three rotating arenas** that swap every 5 waves for visual progression — a **jungle pit**, an underground **crystal cave**, and an organic alien **hivemind**.
- **Four enemy types** — swarming bugs, ranged flyers, stationary artillery that lobs telegraphed shells, and **three unique bosses** (Hive Queen, Brood Tank, Spire Wraith) with ranged + AoE attacks and health bars.
- **Four weapons on a progression** — pulse rifle, auto shotgun, machine gun, grenade launcher — each unlocked by defeating a boss, each with its own ammo type.
- Endless difficulty scaling, **persistent high score**, pause screen, end-of-run stats, hit feedback, and an **adaptive 3-track procedural soundtrack**.
- **100% procedural** — every model, level, sound effect, and the music are generated in code. No external art or audio.

## Controls

- **WASD** move · **Mouse** look · **Click** fire · **E** sprint · **Space** jump
- **1–4** swap weapon · **P** pause · **M** mute · **Esc** release mouse

## Tech

- [Three.js](https://threejs.org/) (WebGL), loaded via CDN import map — no bundler.
- Procedural voxel art (everything is colored boxes), procedurally built levels, and the [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API) for every sound effect and the soundtrack.
- ~1,800 lines of vanilla JavaScript in a single `index.html`.

## Run locally

It uses ES modules, so it must be served over http (not opened as a `file://`):

```bash
python3 -m http.server 8090
# then open http://localhost:8090
```
