# Ahrens Zettelkasten Vault (Kepano layer)

A Zettelkasten vault built around Sönke Ahrens' *How to Take Smart Notes*, with Kepano's categories and base files powering the dashboards. Six folders, six templates, five base views.

## The book

**Sönke Ahrens, *How to Take Smart Notes: One Simple Technique to Boost Writing, Learning and Thinking* (Polity Press, 2017).** The book explains why the Zettelkasten works and exactly how to run one: fleeting notes capture, literature notes translate sources into your own words, permanent notes carry one idea each, and the slip-box turns them into writing. This vault is that method translated to Obsidian.

- Author's website: https://www.soenkeahrens.de/
- Get the book: [ebook on Amazon](https://www.amazon.com/How-Take-Smart-Notes-Technique-ebook/dp/B09V5M8FR5) · [audiobook on Audible](https://www.audible.com/pd/How-to-Take-Smart-Notes-Audiobook/B0DXQYJ2ZS)

The book is short, and reading it beats any template: the vault gives you the structure, the book gives you the why.

## Resources: Sönke Ahrens in conversation

Podcast episodes featuring the author after the book's publication:

- **The Informed Life**, Episode 122: "Sönke Ahrens on Smart Notes" (September 2023) — notes, thinking, and learning through the zettelkasten. https://theinformed.life/2023/09/10/episode-122-soenke-ahrens/
- **Coaching for Leaders**, Episode 564: "Make Your Reading More Meaningful, with Sönke Ahrens" (January 2022) — turning reading into notes that fuel writing and thinking. https://coachingforleaders.com/podcast/make-reading-more-meaningful-sonke-ahrens/
- **The Unmistakable Creative**: "The Knowledge Management Series: Sönke Ahrens | How to Take Smart Notes" (October 2022) — the method, the science behind it, and how to apply it. https://shows.acast.com/the-unmistakable-creative-podcast/episodes/the-knowledge-management-series-sonke-ahrens-how-to-take-sma

## What this vault adds

Kepano's categories and base files on top of the method: category pages, dashboard views per folder, and templates that file a note onto the right dashboard automatically.

- **Category linking, not folders, is what most Bases filter on.** A note belongs to a stage because its frontmatter `categories` field links to a page in `categories/`, e.g. `categories: ["[[literature]]"]`, not because of where the file sits. The exception is `01 queue.base`, which filters by folder (`00 inbox`) directly, since inbox notes are meant to be format-free and often lack frontmatter entirely.
- **Templates** (`50 templates/`) set the `categories` link automatically, so creating a note from the right template is what puts it on the right dashboard. Six templates: fleeting, literature, permanent, project, plus `recipe.md` and `my-note.md`, deliberately outside this system.

## Folder structure

| Folder | Base | Rule |
|---|---|---|
| `00 inbox` | `01 queue.base` | Empty it daily. Nothing here is finished. |
| `10 literature` | `01 library.base` | One idea per note, in your own words, never copied. |
| `20 slip-box` | `01 moc.base`, `02 related.base` | One idea per note, linked to what it relates to. Never archived. |
| `30 projects` | `01 tracker.base` | One subfolder per project. References the slip-box, doesn't absorb it. |
| `40 archive` | — | Finished projects only. Not a home for literature or permanent notes. |
| `50 templates` | — | Note formats, including `recipe.md` and `my-note.md`. |

Each folder starts with `00 guide.md`, its rulebook; read it before working in the folder.

## Requirements and setup

1. Obsidian 1.9+ (Bases is a core plugin; built and tested on 1.13.4).
2. Enable Templates (Settings → Core plugins) and set its template folder to `50 templates`.
3. Bases is on by default in 1.9+. No configuration needed.

## Credits

Method: Sönke Ahrens, *How to Take Smart Notes*. Categories and base files: kepano (https://github.com/kepano/kepano-obsidian). The Map of Content (MOC) and related-notes pattern is a community adaptation, not from either source specifically. CC BY 4.0.

Prefer the plain method without dashboards? See the stock Ahrens version: https://github.com/rgtdnl/obsidian-ahrens-zettelkasten
