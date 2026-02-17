# 💀 Ground Zero

**AI-powered zombie apocalypse survival RPG — one HTML file, no server required.**

A tabletop-style D20 survival game that runs entirely in your browser. Build a party of up to 4 survivors, manage a base camp of up to 12, and try to stay alive. Choose from 15+ zombie universe presets (Walking Dead, Last of Us, 28 Days Later, Resident Evil, and more) or build your own apocalypse from scratch.

The offline narrator keeps the story going anywhere. On HTTPS (GitHub Pages), an optional on-device AI narrator powered by WebAssembly brings the world to life with zero cloud dependency.

---

## Play Now

**[Play Ground Zero](https://pnmcguire480.github.io/ground-zero-rpg/)** — no install, no download, just play.

Or download `index.html` and open it directly. Everything works offline.

---

## Features

**🎲 Full D20 System** — Six attributes, 25+ skills, 4d6 character creation, skill progression through use. Every action is a roll.

**👥 Party & Base Management** — Lead an active party of up to 4 into the field. Manage up to 12 survivors total at base camp with assignments (guard, forage, scavenge, build, patrol). Base characters act autonomously with behind-the-scenes rolls affected by morale and loyalty.

**🧟 15+ Zombie Presets** — Walking Dead, Last of Us, 28 Days Later, Resident Evil, Train to Busan, World War Z, Evil Dead, Zombieland, and more. Each preset configures infection origin, transmission vectors, zombie types, speed, intelligence, and world rules.

**🔧 Custom Apocalypse Builder** — Don't like presets? Build your own from 100+ options across 16 categories: virus/fungus/nano-tech origins, bite/spore/airborne vectors, shambler-to-apex zombie types, horde behaviors, cure possibilities, and collapse timelines.

**📍 Real-World Locations** — Enter your address and the game pulls actual nearby landmarks via OpenStreetMap. Your local pharmacy, hospital, and hardware store become scavenging zones. Or generate a procedural fictional city from 120+ unique location names.

**🏗️ Base Building** — Barricades, rain collectors, food storage, med stations, watchtowers, workshops. Gather materials, build structures, improve your camp's defense and sustainability.

**⚔️ Tactical Combat** — Encounter-based combat against 8 enemy types with behavior AI (rush, ambush, flee, ranged). Attack, defend, flee, or use items. Critical hits and misses. XP rewards.

**🧠 AI Narrator** *(optional, HTTPS only)* — On-device LLM via WebAssembly (SmolLM2 1.7B). Downloads once (~1 GB), runs forever with no internet. The AI narrates every action, combat, and story beat in the tone of your chosen zombie universe. Falls back to a rich offline narrator when AI isn't available.

**💾 Save System** — Autosave, 3 manual save slots, JSON export/import, undo last turn. Old save formats auto-migrate.

**📱 Mobile-First PWA** — Designed for phones. Installable as an app. Works offline after first load.

---

## Architecture

Ground Zero is built as a **genre-agnostic engine** with a zombie theme layer on top. The D20 system, party management, action economy, combat, base building, and narration pipeline are designed to be reused across future genres (fantasy, sci-fi, espionage, and more) by swapping content packs.

Single-file HTML/CSS/JS. No build tools, no dependencies, no frameworks. Open the file and play.

---

## Tech

- **Single-file HTML5** — ~200KB, everything inline
- **Zero dependencies** — no npm, no build step, no CDN required for gameplay
- **PWA** — installable, offline-capable, data URI manifest and icon
- **Wllama** (optional) — llama.cpp compiled to WebAssembly for on-device AI
- **OpenStreetMap Overpass API** (optional) — real-world location data
- **localStorage** — saves, settings, autosave

---

## Running Locally

Just open the HTML file in any modern browser. For AI narrator features, serve over HTTPS:

```bash
# Quick local server (Python)
python3 -m http.server 8000

# Then open http://localhost:8000/index.html
```

Or push to GitHub Pages for free HTTPS hosting.

---

## Roadmap

- [ ] Base auto-actions with intervention system (death saves for endangered NPCs)
- [ ] Multi-character combat (party members take individual turns)
- [ ] Recruitment system (find and recruit survivors during gameplay)
- [ ] Relationship and loyalty dynamics between survivors
- [ ] Genre spine extraction for future theme packs
- [ ] Fantasy, sci-fi, espionage, and other genre modules

---

## License

MIT
