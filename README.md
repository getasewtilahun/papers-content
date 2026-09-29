# Papers Content Library

Open archival repository containing structured theological papers, patristic studies, essays, lectures, and monographs for the **Papers** application.

---

## Repository Structure

```
├── catalog.json                       # Central library manifest listing all published works
├── nature-of-christian-worship.json   # Structured work with chapters, sections, and blocks
├── life-of-st-basil.json
├── early-church-fathers.json
├── hesychasm-contemplation.json
├── patristic-doctrine-creation.json
├── scripture-and-tradition.json
├── content/                           # Mirrored directory for backward compatibility
└── source/                            # Optional source PDFs for archival reference
```

---

## Live Sync

The Papers app directly streams content from this repository via GitHub Raw Fastly CDN:
- `https://raw.githubusercontent.com/getasewtilahun/papers-content/main/catalog.json`
- `https://raw.githubusercontent.com/getasewtilahun/papers-content/main/<work-id>.json`

Any commit to this repository immediately updates the library for all readers worldwide.
