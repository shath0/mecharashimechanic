# Mecharashi Command Library

A single-file, offline **build-guide generator** and **Armed Conquest boss manual** for the mecha tactics gacha *Mecharashi*. No install, no dependencies, no tracking — just open the HTML.

> Unofficial fan project. Not affiliated with or endorsed by the developers of Mecharashi. Data reflects the CN build and shifts with patches — verify against the live game.

## What's inside

The library has two tools behind a top switcher:

### 🛠️ Loadout Terminal
Pick a **pilot** + a **chassis (ST)** and it assembles a full build readout:

- **Suitability** — reads the ST ↔ pilot compatibility map; recommended pairings score higher, off-list combos fall back to a tier-based judgement.
- **Chips** — rules engine: main attribute = pilot weapon type, defensive line = Dodge (Light/Medium) or Crit RES (Heavy), Hit/Crit line = the matching Crit+. Auto-fills from data; overrides for edge cases.
- **Modules** — top-pick → candidate module sets per chassis, with set-bonus and rainbow-effect notes.
- **Weapons** — each pilot's signature-weapon talent (the endgame target), plus full loadouts where documented.
- **Enhancement & Rolls** — the chip enhancement pipeline, sub-stat targeting, sector CP builds, and weapon-tuning notes (weapons have fixed stats; "reroll for perfect stats" = accessory tuning).
- **R&D** — priority class tree + Feature focus for the selected pilot, plus where to farm.
- **Accessories** — trigger/reaction templates by role, the 4 weapon modifications, and a full glossary.
- **Backpacks** — role-based pick, the effect pool, and how the Rank-2 combine system works.

Every field is tagged **verified** (read from source), **inferred** (from role/type patterns), or **v2** (not yet transcribed), so you always know how much to trust it.

### ⚔️ Armed Conquest — Field Manual
The endgame mode, made legible so you don't have to scrub through videos:

- **How the mode works** — locked pilots, bounties, mercenaries, weekly reset, challenge budget.
- **Unlock requirements & progression** — per-section gates, difficulty structure, rewards.
- **Universal tactics** — the transferable principles that win most stages.
- **Per-boss briefs** — 19 bosses across the first five sections, each with bounties, a quick reference, the threat, how to beat it, recommended pilots, and Extreme-mode notes. Later sections carry what's confirmed so far.

## Use it

- **Locally:** open `index.html` in any modern browser. It's fully self-contained and works offline.
- **On the web (GitHub Pages):** push this repo, then **Settings → Pages → Deploy from branch → `main` / root**. Your library goes live at `https://<you>.github.io/<repo>/`.

The two tools also exist as standalone files in [`/standalone`](./standalone) if you ever want them separately.

## Extending it

Everything is a plain data object near the top of the relevant `<script>` block — no framework, no build step. Add a pilot or chassis = add one entry to `PILOTS` / `STS`; add a boss = add an entry to `SECTIONS`. The render logic picks it up automatically.

## Credits & sources

- **Loadout data** — the community *"Michu Wiki Mecharashi"* spreadsheet by **MICHUZAK** (tier lists, ST↔pilot compatibility, module sets, accessories, backpacks, signature weapons, chip rules).
- **Weapon stats & modification system** — iFanzine and community weapon guides.
- **R&D** — official patch notes / store update text, GamingonPhone, and community Steam discussions.
- **Armed Conquest** — CarlosPenaJr's *"Armed Conquest Battles"* Steam guide, treyexgaming's Armed Conquest guide, and demonstration videos from the **MICHUZAK** YouTube channel.

Strategy text is paraphrased and condensed; rankings reflect their authors' opinions. All game names, art, and data belong to the game's developers and the respective guide authors.

## License

Tool code: [MIT](./LICENSE). Game data and strategy write-ups remain the work of their respective community authors (see credits). Remember to drop your name into the `LICENSE` file.
