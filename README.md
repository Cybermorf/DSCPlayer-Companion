# DSC Player Companion

Player-facing companion for **The Dark Sun Chronicles**. Create and manage characters, browse DSC classes, log sessions, keep notes, roll dice, and sync **spells & equipment** from Open5e / SRD.

> DM tools (bestiary, combat tracker, factions, Dynamic Influence Engine) live in the separate [DSCToolkt](https://github.com/Cybermorf/DSCToolkt) repo.

## Features

| Section | What you get |
|--------|----------------|
| **Campaigns** | Personal campaign slots (shared table name is fine) |
| **Sessions** | Session log — date, title, summary |
| **Characters** | Full character creation & sheets (races, classes, Moon Guardian paths, point buy / standard array, equipment, spells, Umbrarian template, avatar, view / print / export) |
| **DSC Classes** | Moon Guardian & other DSC class details and progression |
| **Notes** | Free-form campaign notes (auto-save) |
| **Tools** | Dice roller · JSON compendium import · **Open5e v2 sync (spells + equipment only)** |
| **Dice** | Always available from the header |

Character features match the DM toolkit: armor AC, inventory equip, spell cards, Umbrarian Shard DC, A4 print, etc.

## Quick start

```bash
# serve locally
python -m http.server 8080
```

Or open `index.html` directly. Data is stored in this browser only (`localStorage` + IndexedDB for compendium).

## Open5e / SRD sync

1. Open **Tools**
2. Optionally keep **SRD 5.2 only** checked
3. **Sync Spells + Equipment** (or Spells / Weapons & Armor alone)

Uses `https://api.open5e.com/v2`. Large catalogs store in **IndexedDB**.

## Deploy (GitHub Pages)

Settings → Pages → GitHub Actions (workflow included), or publish the repo root as static files.

## Related

- DM Companion: https://github.com/Cybermorf/DSCToolkt

## Attribution

SRD / Open5e material under the licenses of those sources (including CC-BY-4.0 for Wizards SRD content where applicable). Dark Sun Chronicles materials for the owning table.

---

*The Dark Sun Chronicles · Player Companion*
