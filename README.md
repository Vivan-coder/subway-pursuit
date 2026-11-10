# Subway Pursuit

An endless runner where you are the cop chasing the kid.

## Play

Open `index.html` in any modern browser. No build step, no dependencies.

## Controls

| Action | Keyboard | Touch |
| --- | --- | --- |
| Switch lanes | Left / Right or A / D | Swipe left / right |
| Jump | Up, W or Space | Swipe up |
| Roll (fast-fall in air) | Down or S | Swipe down |
| Pause | P or Esc | Pause button |
| Mute | M | - |

## Gameplay

- A chase meter shows the gap between you and the kid.
- Coins close the gap. Crash twice within a few seconds and he escapes.
- Close the gap to 2 m to bust him and move on to a faster kid.
- There are 5 levels. Each one is a tougher kid on a tougher route.
- Level 3 is a mini-boss and level 5 is the final boss, Big Brat.

## Obstacles

- Trains block a lane
- Low barriers (jump)
- Overhead bars (roll)
- Open pits (jump)
- Cones (small stumble)
- Oil slicks (sluggish steering)
- Gauntlet rows that chain a jump and a roll

## Pickups

- Turbo: invincible and fast, smashes through obstacles
- Magnet: pulls coins toward you
- Shield: absorbs one hit
- Taser: stuns the kid and closes the gap
- Donut: closes the gap and adds bonus points

## The kid

He is not nice. He throws trash cans, bottles, paint balloons and skateboards at you,
drops oil and cones, dashes ahead to show off, and taunts you the whole way.

## Run locally with a server

```
npm start
```

or

```
python -m http.server 8000
```

## Tech notes

- Plain HTML + Canvas 2D, no libraries
- Pseudo-3D perspective projection with depth sorting
- Procedural audio with the Web Audio API
- Best score is saved in `localStorage`

## License

MIT, see [LICENSE](LICENSE).

## Levels

| # | Name | Theme | Notes |
| --- | --- | --- | --- |
| 1 | Sunset Station | Golden hour | Gentle warm-up |
| 2 | Neon Night | Neon city | Faster kid, more attacks |
| 3 | Rainy Docks | Rain | Mini-boss: Skate King (2 tackles) |
| 4 | Storm Yard | Storm and lightning | Double throws, gauntlet rows |
| 5 | Midnight Showdown | Blood-red night | Final boss: Big Brat (4 tackles) |

Levels unlock strictly one after the other: you must catch the kid to unlock the next level. Progress is saved in `localStorage`.

## Shop

Coins you collect go into a persistent wallet. Spend them in the shop between levels,
from the main menu (S) or from the game over screen.

Upgrades (5 tiers each, 100 / 220 / 400 / 650 / 1000 coins): Turbo, Magnet, Shield, Taser, Donut, Cardio, Lucky Badge.

Boosts (single use, max 5 each): Head Start (150), Ready Shield (100), Coin Doubler (200).

Power-ups are intentionally modest, so maxing everything takes many runs.

## More features

- Voiced kid: he actually speaks his taunts using the browser's speech synthesis (V toggles voice, M mutes everything)
- Jetpack pickup: fly over everything for a few seconds
- Coin combo multiplier (up to x5)
- Two missions per level that pay bonus coins
- The kid climbs onto train roofs or dodges around them
