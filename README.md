# aOS-ppt-design

A Claude Code plugin that makes Claude build PowerPoint slides in the AthleteOS brand. It holds one skill, `athleteos-design-kit`: design guidance taken from the AthleteOS marketing website and translated into slide terms, with the logo and font files a deck needs.

## Install

The plugin is listed in the `athleteOS-plugins` marketplace, which lives in `lgerard314/athleteOS-marketplace`. Both repositories are private, so the machine needs git access to them.

```text
/plugin marketplace add lgerard314/athleteOS-marketplace
/plugin install aos-ppt-design@athleteOS-plugins
```

Then ask for a slide or a deck for AthleteOS. Claude loads the skill on its own, or you can call it as `/aos-ppt-design:athleteos-design-kit`.

## Use it without Claude Code

The skill folder works by itself. To add it to claude.ai as a custom skill, zip `skills/athleteos-design-kit` so that the zip contains the folder itself, and upload the zip where custom skills are added in Settings. In a single chat, attach `skills/athleteos-design-kit/SKILL.md` and the logo PNG for the background you want.

## What is in the skill

| Path under `skills/athleteos-design-kit/` | What it is |
|---|---|
| `SKILL.md` | The guidelines: colour, type, layout, shapes, photography, logo, wording, and a checklist |
| `logo/` | The wordmark for ink, paper and red backgrounds, and the monogram, as PNG and SVG |
| `fonts/` | Big Shoulders Display (Bold, ExtraBold) and Barlow (Regular, Medium), with their licences |
| `reference/site-screenshots/` | The website, section by section, as the visual source of the look |

## Install the fonts

PowerPoint only shows a typeface that is installed on the machine. Install the four `.ttf` files in `skills/athleteos-design-kit/fonts/` on every computer that will edit or present the decks, then restart PowerPoint. The names the files declare, and that `SKILL.md` tells Claude to use, are `Big Shoulders Display`, `Big Shoulders Display ExtraBold`, `Barlow` and `Barlow Medium`; if PowerPoint's font list shows one differently on your machine, tell Claude the name it shows. Both families are under the SIL Open Font License, included beside them, which allows installing, embedding and passing them on. To send a deck to someone without the fonts, export it as a PDF.

## Releasing a change

`version` in `.claude-plugin/plugin.json` is what an installed copy is held to. After changing anything, raise it, or `/plugin update` reports the plugin as already up to date and nobody receives the change.

## What is AthleteOS's own

The logo files are the company's mark, and the screenshots show the company's website, its words and its photographs. They are here so slides for AthleteOS can be made correctly, and are not for use on anything else.
