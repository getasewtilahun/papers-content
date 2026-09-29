# Papers Content Library

Open archival repository containing structured theological papers, patristic studies, essays, and lectures for the **Papers** application.

---

## Content Format

All works are published as **pure structured JSON** files:

```
├── catalog.json                       # Central library manifest listing all published works
├── nature-of-christian-worship.json   # Structured work with chapters, sections, and blocks
├── life-of-st-basil.json
├── early-church-fathers.json
├── hesychasm-contemplation.json
├── patristic-doctrine-creation.json
└── scripture-and-tradition.json
```

---

## Adding a New Paper

### 1. Register in `catalog.json`

Add a new metadata object to the `catalog.json` array:

```json
{
  "id": "my-new-paper",
  "title": "Title of the Theological Work",
  "author": {
    "id": "author-id",
    "name": "Author Full Name",
    "bio": "Biographical summary",
    "era": "e.g. 4th Century or 20th Century"
  },
  "type": "Paper",
  "category": "Theology",
  "shortDescription": "One or two sentence summary of the paper.",
  "publicationInfo": "Original journal or patristic volume citation.",
  "estimatedReadingMinutes": 25
}
```

### 2. Create the Structured File (`<work-id>.json`)

Create `<work-id>.json` at the root with structured chapters, sections, and blocks:

```json
{
  "id": "my-new-paper",
  "title": "Title of the Theological Work",
  "author": {
    "id": "author-id",
    "name": "Author Full Name"
  },
  "type": "Paper",
  "category": "Theology",
  "chapters": [
    {
      "id": "chap-1",
      "number": 1,
      "title": "Chapter or Section Title",
      "sections": [
        {
          "id": "sec-1-1",
          "title": "Subheading Title",
          "blocks": [
            {
              "type": "paragraph",
              "text": "Body text formatted for serene, justified reading."
            },
            {
              "type": "blockquote",
              "text": "Extracted theological or patristic quotation."
            },
            {
              "type": "footnote",
              "noteId": "1",
              "text": "Scholarly citation or reference automatically displayed in the paper page footer."
            }
          ]
        }
      ]
    }
  ]
}
```

### Supported Block Types

- `paragraph`: Standard body text (rendered justified in archival serif typography).
- `blockquote`: Quotation with left vertical accent bar.
- `heading` / `subheading`: Section headers.
- `footnote` / `reference`: Citations automatically placed in the paper page sheet footer.
- `image`: Archival illustrations with optional `caption` and `alt`.

---

## Live Sync

The Papers app directly streams content from this repository via GitHub Raw Fastly CDN:
- `https://raw.githubusercontent.com/getasewtilahun/papers-content/main/catalog.json`
- `https://raw.githubusercontent.com/getasewtilahun/papers-content/main/<work-id>.json`

Committing a new paper here instantly delivers it to readers worldwide.
