# Portfolio — ex-machina-2030

## Quick start

Push this entire folder to your GitHub repo. Enable GitHub Pages on `main` branch, root `/`.

## Structure

```
/
├── index.html          ← Portfolio page (never edit this)
├── projects.json       ← ADD NEW PROJECTS HERE
├── README.md
└── apps/
    └── gpay-budget/    ← One folder per project
        ├── index.html  ← Case study template (never edit)
        ├── content.json← EDIT THIS for case study content
        └── cover.svg   ← Thumbnail image
```

## Adding a new project (2 steps)

### Step 1 — Add a tile to the portfolio

Open `projects.json` and add an entry:

```json
{
  "id": "my-new-project",
  "title": "Project Title",
  "subtitle": "One-line description",
  "thumbnail": "apps/my-new-project/cover.png",
  "tags": ["UX", "Research"],
  "year": "2026"
}
```

- `id` must match the folder name under `apps/`
- `thumbnail` is optional — if missing, the title is shown as text
- `subtitle`, `tags`, `year` are all optional

### Step 2 — Create the case study

1. Copy `apps/gpay-budget/` as a template
2. Rename the folder to match your `id`
3. Edit `content.json` inside it:

```json
{
  "title": "Project Title",
  "subtitle": "Subtitle",
  "role": "Your role",
  "timeline": "When",
  "overview": "Summary paragraph",
  "sections": [
    {"heading": "Section Title", "body": "Content..."}
  ],
  "links": [
    {"label": "Prototype", "url": "https://...", "type": "prototype"},
    {"label": "Research Doc", "url": "https://...", "type": "doc"},
    {"label": "Slides", "url": "https://...", "type": "slides"}
  ],
  "prototype_embed": "https://url-to-embed-in-iframe"
}
```

4. Add a cover image (PNG, JPG, or SVG) to the folder
5. Commit and push — done

## Link types for resources

- `prototype` → ◎ icon
- `doc` → 📄 icon  
- `slides` → 📊 icon
- `sheet` → 📋 icon
- anything else → → arrow icon

## Custom domain

If using `apps.ex-machina-2030.com`, set CNAME in GitHub Pages settings.

## Notes

- The portfolio page reads `projects.json` at runtime — no build step
- Case study pages read their own `content.json` — no build step
- You never need to edit any HTML file
- Just edit JSON files + add images, commit, push
