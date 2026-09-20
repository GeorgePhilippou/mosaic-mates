# Mosaic Mates

An original, iPad-first block-placement puzzle inspired by the satisfying spatial planning of modern block games.

## Prototype 0.2

- 8×8 board and three-shape tray
- Tap a shape, then tap its top-left board position
- Row and column clears
- Escalating glow/combo bonus
- Solo Glow, Shared Spark, and Score Race modes
- Local best scores and offline PWA shell
- Private-room host/join interface and synchronized online game engine

## Product direction

The target experience is a private two-iPad game for George and Megan. The online engine uses anonymous authenticated realtime rooms, synchronized seeded piece generation, transactional moves, and reconnect-safe shared state. It deliberately does not reuse another game's Firebase project.

The dedicated `mosaic-mates-george` Firebase project and Web App are registered. To activate rooms, enable Anonymous Authentication, create the default Realtime Database in `europe-west1`, and deploy `database.rules.json`.

Planned online modes:

1. **Shared Spark** — one shared board, private piece trays, alternating or simultaneous play, and a shared timer.
2. **Score Race** — identical piece sequence on separate boards; highest score after three minutes wins.
3. **Rescue** — separate boards with team clears that charge gifts such as a single-cell piece or board shuffle.

## Run locally

From this folder:

```sh
python3 -m http.server 8765
```

Then open `http://localhost:8765`.
