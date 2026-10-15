# DSC Player Companion

Player-facing companion for **The Dark Sun Chronicles**. Create and manage characters, browse DSC classes, log sessions, keep notes, roll dice, and sync **spells & equipment** from Open5e / SRD.

DM-only tools (bestiary, combat tracker, factions, DIE) live in **[DSCToolkt](https://github.com/Cybermorf/DSCToolkt)**.

**Repo:** https://github.com/Cybermorf/DSCPlayer-Companion

---

## Quick start

```bash
python -m http.server 8080
# → http://localhost:8080
```

Or open `index.html` directly. Data stays in this browser (`localStorage` + IndexedDB for compendium).

**Hard refresh after updates:** `Ctrl+Shift+R` (Windows/Linux) or `Cmd+Shift+R` (Mac)

---

## Sections

| Section | What you get |
|--------|----------------|
| **Campaigns** | Personal campaign slots |
| **Sessions** | Session log — date, title, summary |
| **Characters** | Full character creation & sheets (see below) |
| **DSC Classes** | Moon Guardian & DSC class details / progression |
| **Notes** | Free-form notes (auto-save) |
| **Tools** | Dice · JSON import · **Open5e v2 sync (spells + equipment only)** |
| **Dice** | Always available from the header |

Villains / combat / bestiary are **not** included (DM Toolkit only).

---

## Character sheets

Matches the DM toolkit feature set for PCs:

- **Races:** DSC · Official 5e · Homebrew/Imported  
- **Classes & multiclass** (PHB rules; Level Up button; subclasses gated by class level)  
- **ASI / Feats:** stacked per-class slots; +2 stats or one feat; Feats list assigns to next open ASI slot  
- **Skills:** limits from each class when multiclassing  
- **Ability scores:** manual, point buy, standard array  
- **Equipment & inventory** (search, equip → AC/attacks)  
- **Spells** (slots, cards, preparation mode)  
- **Class resources** (Ki, Lunar Charges, etc.)  
- **Umbrarian:** only if imported from DM with the template active; player can adjust stage/corruption only  
- **View / Print** (Combat → Attacks & Spells → Progression → Story)  
- **Export / Import JSON** with stable `characterId` — re-import **updates** an existing sheet  

### Sheet lock
If the DM locked the sheet on export/save, the Player app can only edit:

- Equipment & inventory  
- HP / conditions  
- Level Up & multiclass levels  
- Unclaimed ASI / Feat slots  

Race, base ability scores, background, and free-form locked fields require the DM.

---

## Open5e / SRD sync

1. Open **Tools**  
2. Optionally keep **SRD only** checked  
3. **Sync Spells + Equipment** (or spells / gear alone)

Uses `https://api.open5e.com/v2`. Large catalogs go to **IndexedDB**.  
Bestiary / creatures are **not** imported on the Player app.

---

## Character ID

Each character has a hidden stable `id` (exported as `characterId`).  
Importing the same file again updates that character instead of creating a duplicate.

---

## Deploy (GitHub Pages)

Settings → Pages → GitHub Actions, or publish the repo root as static files.

**From release zip:** extract so `index.html` is at the site root.

---

## Related

- DM Companion: https://github.com/Cybermorf/DSCToolkt

## Attribution

SRD / Open5e under their respective licenses. Dark Sun Chronicles materials for the owning table.

---

*The Dark Sun Chronicles · Player Companion*


### Custom packs from the DM

Import a `DSCToolkt-compendium-v2` JSON from the DM Toolkit (**Export Custom Pack**):

- **Supported:** spells, equipment, races, classes, subclasses, feats  
- **Not imported:** creatures / bestiary (DM-only)

Use **Tools → Import** / Open5e section’s JSON import control.
