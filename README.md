# TollUp

A kid-friendly 3D first-person brawler that runs in the browser on computers and phones.

Pick a hero, jump into a 1v1, 2v2, 3v3 or Squad (4v4) match, and bonk the other team until their HP runs out. The winner does a special victory move.

## Heroes

| Hero | Class | HP | Style | Victory move |
|---|---|---|---|---|
| Brick | Tank | 300 | Slow, heavy hits | Ground Pound |
| Nova | Balanced | 200 | Good at everything | Star Spin |
| Zip | Fast | 150 | Very quick combos | Flip Flash |

## Controls

**Computer:** WASD or arrow keys to move, mouse to look (click the game first), Space to jump, left click or F to hit, Esc to free the mouse.

**Phone or tablet:** drag on the left side to move, drag on the right side to look, tap HIT (hold to keep swinging) and JUMP.

## Progress and rewards

- Every match gives XP and coins, and wins give trophies.
- Wins unlock skins and mascots: 1v1 drops Common, 2v2 Rare, 3v3 Epic, Squad Legendary.
- Common, Rare and Epic items can also be bought with coins in the Locker.
- The leaderboard ranks players by trophies.

## Online play

The first 3 games are warm-ups against bots. After that, TollUp looks for real players and fills empty spots with bots.

Matchmaking, friends and the shared leaderboard use the Claude artifact runtime (`window.claude`: `room`, `db` and `user`). Opened anywhere else, such as GitHub Pages or a local file, the game still runs fully offline against bots and saves progress in the browser.

## Tech

One self-contained `index.html`: Three.js r128 (loaded from cdnjs) for the 3D graphics and the Web Audio API for all sound effects and music, which are generated in code. No build step.
