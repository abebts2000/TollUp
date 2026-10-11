# TollUp

A kid-friendly top-down 3D arena brawler with realistic lighting, textures and foliage. It runs in the browser on computers and phones.

Pick a hero, jump into a 1v1, 2v2, 3v3 or Squad (4v4) match, and bonk the other team until their HP runs out. The winner does a special victory move.

## Heroes

| Hero | Class | HP | Style | Victory move |
|---|---|---|---|---|
| Brick | Tank | 300 | Slow, heavy hits | Ground Pound |
| Nova | Balanced | 200 | Good at everything | Star Spin |
| Zip | Fast | 150 | Very quick combos | Flip Flash |

## Controls

**Computer:** WASD or arrow keys to move, point the mouse to aim, left click or F to attack, Q or right click for your Super, E for your gadget, Space to jump.

**Phone or tablet:** drag on the left side to move. Drag the red stick to aim and let go to attack (tap it to auto-aim). The yellow stick fires your Super once it's charged. Gadget and JUMP buttons sit above.

## Ammo, Super and bushes

- Each attack uses one of 3 ammo bars, which refill over time.
- Landing hits charges your Super: Brick's Boulder Slam, Nova's Star Burst (spin plus heal) or Zip's Zip Dash.
- Enemies standing in bushes are invisible until you get close or they attack.

## Gadgets

Run into a glowing box in the arena to grab a gadget, then use it with **E**, right click, or the gadget button on phones.

| Gadget | What it does |
|---|---|
| Turbo Sneakers | Run 50% faster for 6 seconds |
| Boing Boots | Jump much higher for 8 seconds |
| Bubble Shield | Blocks every hit for 5 seconds |
| Mega Mitts | Hit 60% harder for 7 seconds |
| Snack Pack | Heals 35% of your HP |
| Freeze Blaster | 3 ice shots that slow whoever they hit |

## Arena

- A spinning sweeper bar in the middle knocks you away if you don't jump over it.
- Green bounce pads launch you onto the tall crates.
- Crates, walls, stone pillars and barrels give you cover.

## Fullscreen on phones

On phones the game asks you to go fullscreen before a match. On iPhone, where browsers can't go fullscreen, add TollUp to your home screen (Share → Add to Home Screen) and open it from there.

## Progress and rewards

- Every match gives XP and coins, and wins give trophies.
- Wins unlock skins and mascots: 1v1 drops Common, 2v2 Rare, 3v3 Epic, Squad Legendary.
- Common, Rare and Epic items can also be bought with coins in the Locker.
- The leaderboard ranks players by trophies.

## Online play

The first 3 games are warm-ups against bots. After that, TollUp looks for real players and fills empty spots with bots.

Matchmaking, friends and the shared leaderboard use the Claude artifact runtime (`window.claude`: `room`, `db` and `user`). Opened anywhere else, such as GitHub Pages or a local file, the game still runs fully offline against bots and saves progress in the browser.

## Tech

One self-contained `index.html`: Three.js r128 (loaded from cdnjs, with its bloom post-processing from jsDelivr) for the 3D graphics and the Web Audio API for all sound effects and music, which are generated in code. No build step.
