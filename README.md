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
- Every third chase is a boss fight against Big Brat.

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
