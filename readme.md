# obsidian vault for beginners

A Zettelkasten vault built around Sönke Ahrens' *How to Take Smart Notes*, with Kepano's categories and base files for the dashboards.

https://www.amazon.com/How-Take-Smart-Notes-Technique-ebook/dp/B09V5M8FR5

```
00 inbox      unprocessed captures, cleared daily
10 literature translated notes from sources (books, papers, articles, podcasts, videos)
20 slip-box   permanent notes and their connections
30 projects   active writing, one folder per piece
40 archive    finished projects
50 templates  note formats
categories    category pages that back the Bases views
```

## Requirements

- Obsidian 1.9+ (Bases is a core plugin; built and tested on 1.13.4)
- Core plugins enabled: **Bases**, **Templates**

## Setup

1. Enable Templates (Settings → Core plugins) and set its template folder to `50 templates`.
2. Bases is on by default in 1.9+. No configuration needed.

## How it works

Each numbered folder starts with `00 guide.md`, its rulebook. Read the `00 guide.md` in a folder before working in it; the rules are specific per stage (e.g. inbox notes get deleted within 1–2 days, permanent notes never get archived). The folder's `01 …base` file (and `02 related.base` in the slip-box) is its dashboard view.

**Category linking**, not folders, is what most Bases filter on. A note belongs to a stage because its frontmatter `categories` field links to a page in `categories/`, e.g. `categories: ["[[literature]]"]`, not because of where the file sits. The exception is `01 queue.base`, which filters by folder (`00 inbox`) directly, since inbox notes are meant to be format-free and often lack frontmatter entirely.

**Templates** (`50 templates/`) set the `categories` link automatically, so creating a note from the right template is what puts it on the right dashboard. There are six: fleeting, literature, permanent, project, plus `recipe.md` and `my-note.md`, which are deliberately outside this system: free-form notes that won't appear in any Base.

## Folders

| Folder | Base | Rule |
|---|---|---|
| `00 inbox` | `01 queue.base` | Empty it daily. Nothing here is finished. |
| `10 literature` | `01 library.base` | One idea per note, in your own words, never copied. |
| `20 slip-box` | `01 moc.base`, `02 related.base` | One idea per note, linked to what it relates to. Never archived. |
| `30 projects` | `01 tracker.base` | One subfolder per project. References the slip-box, doesn't absorb it. |
| `40 archive` | — | Finished projects only. Not a home for literature or permanent notes. |

## Credits

Method: Sönke Ahrens, *How to Take Smart Notes*; and kepano's categories and base files (https://github.com/kepano/kepano-obsidian). The Map of Content (MOC) and related-notes pattern is a community adaptation, not from either source specifically.

Prefer the plain method without dashboards? See the stock Ahrens version: https://github.com/rgtdnl/obsidian-ahrens-zettelkasten
