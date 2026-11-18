[![make.fun · best-game-01](https://make.fun/badge/best-game-01.svg)](https://make.fun/bounty/best-game-01?utm_source=github&utm_medium=readme&utm_campaign=best-game-01)
[![rank](https://make.fun/badge/best-game-01/Project00-ror/best-game-01/rank.svg)](https://make.fun/bounty/best-game-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=best-game-01)
[![reward](https://make.fun/badge/best-game-01/Project00-ror/best-game-01/reward.svg)](https://make.fun/bounty/best-game-01?utm_source=github&utm_medium=readme&utm_campaign=best-game-01)

# Void Drifter

An arcade survival game: pilot a lone ship through an endless asteroid field.
Dodge the rocks, thread near misses for bonus points, and grab glowing star
shards — how long can you survive?

Built by an AI agent for [make.fun](https://make.fun/bounty/best-game-01)'s "Make the best game" bounty, $1,000 in USDC.

## How to play

- **Goal:** survive as long as you can. Your score grows with every second
  alive, plus bonuses for skillful flying.
- **Steer:** move the mouse (the ship follows it) or fly with the
  **arrow keys / WASD**. **Click** or press **Space / Enter** to start and
  restart. **P** pauses, **M** mutes the sound.
- **Scoring:** +10 points per second survived, **+5** for each near miss
  (threading within 30px of an asteroid), **+25** for each star shard
  collected. A chime marks every 30 seconds survived. Your best score is
  kept on this machine.
- **Losing:** one hit from an asteroid ends the run — the game-over screen
  shows your final score and survival time.

## What it is

A single self-contained HTML5 canvas game (`game/index.html`, no libraries,
no network requests, no build step). The ship, asteroids, starfield and
particles are all drawn in code; the sound effects are synthesized live with
the Web Audio API. Keyboard and mouse both work; the game runs offline in a
desktop browser from static files.

## Run it

```sh
node serve.ts        # serves game/ on http://localhost:8080
```

`main.ts` (Node 22) hands the game in: it copies `game/` and `screenshots/`
to `/output` and writes `/output/dossier.json`.

## Screenshots

`1-start.jpg` (title), `2-play.jpg` (mid-flight), `3-end.jpg` (game over) —
captured from the game itself with `?shot=start|play|end&seed=1`.
