# Org Topologies — Italian translations (Italiano)

This folder (`it/`) holds the Italian text of [orgtopologies.com](https://www.orgtopologies.com/it).
Edit here; the site picks up the latest version with its next release (usually the same day).

The texts were drafted by AI and are marked `"status": "draft"`. On the site they show a small
“machine-translated, under review” note. Your review turns them into real Italian.

## What to translate

| File | Entries | What it is | On the site |
|---|---|---|---|
| `glossary.json` | 306 | **The termbase. Start here.** Every Org Topologies term: its name and definition. Shown on the Glossary page and in the hover cards on every page. All other files must use these terms. | /glossary |
| `ui.json` | 110 | The site frame: main menu, footer, buttons and small labels used everywhere (map buttons, “See in Glossary →”, “Read the case study →”). | every page |
| `data/katalog.json` | 74 | The Elevating Katas catalog: the five Star Model elements and every kata’s name and one-line summary. | /elevating-katas |
| `pages/home.json` | 39 | The Home page. | / |
| `pages/made.json` | 116 | Approach: the MADE method (Map, Assess, Design, Elevate). | /made |
| `pages/mapping.json` | 125 | Mapping: the map, the two mandates, the four intelligences, how to map your organization. | /mapping |
| `pages/topologies.json` | 169 | The three topologies (Resource, Delivery, Adaptive), fit for purpose, and which frameworks build each. | /topologies |
| `pages/elevating-katas.json` | 64 | Elevating Katas page text around the catalog. | /elevating-katas |
| `pages/glossary.json` | 8 | The Glossary page’s own heading and intro. | /glossary |
| `pages/academy.json` | 12 | The Academy page. | /academy |
| `pages/10xorg.json` | 2 | The book page (10X ORG). | /10xorg |
| `shared/academy.json` | 17 | The Academy block (courses), at the end of most pages. | all pages except the blog |
| `shared/academy-bar.json` | 6 | The small Academy banner. | /made, /mapping, /topologies, /elevating-katas |
| `shared/book.json` | 83 | The 10X ORG book block, with reader reviews. | /, /10xorg |
| `shared/community.json` | 12 | The community / newsletter block. | most pages |
| `shared/elevate-katas.json` | 9 | The Elevating Katas block. | /, /topologies |
| `shared/four-intelligences.json` | 24 | The four intelligences block (Directing, Driving, Doing, Delivering). | /, /mapping |
| `shared/made-overview.json` | 24 | The MADE overview block. | / |
| `shared/map-detail.json` | 35 | The 4×4 map explainer. | /mapping |
| `shared/testimonials.json` | 22 | Quotes from practitioners. | /, /academy |
| `shared/topologies-trio.json` | 24 | The three-topologies cards. | / |
| `maps/*.json` | ~128 | Texts drawn inside the org maps: frame titles, subtitles, unit and flow labels. **Keys are the English text.** Keep them short (they must fit the drawing); axis words, quadrant names, topology names and MADE words stay English. | /, /made, /mapping, /topologies |

Order of work: **`glossary.json` first** (it fixes the terms), then `ui.json`, then the pages you care most about.
The blog and case studies stay in English for now; links to them open the English page.

## The format

Each entry is one line of meaning:

```json
"mandate.term": { "en": "Mandate", "text": "…your translation…", "src": "9f3a1c2e", "status": "draft" }
```

| Field | Meaning | Edit? |
|---|---|---|
| `en` | The English original, for reference | no |
| `text` | The translation | **yes** |
| `src` | Fingerprint of the English (set by the tools) | no |
| `status` | `draft` → change to `reviewed` when you have checked the entry | yes |

The key (e.g. `mandate.term`, `hero.title`) says where the text is used; don't change keys.
When the English changes later, the site keeps showing your text and marks it outdated for an update.

## Never translate or change

- **Org Topologies™** (always in Latin script), **10X ORG**, **MADE**, **C-OTP**, **C-OTC**, **Obeya**, **Aiden**.
- Archetype codes (TASKS-1 … WHOLE-4), names of people and companies.
- Placeholders in braces: `{n}`, `{name}`, `{year}` — keep them exactly; you may move them in the sentence.
- Formatting marks: `**bold**`, `==highlight==`, line breaks (`\n`), arrows `→`.
- Links `[text](target)`: translate the text, **never the target** (e.g. `[マンデート](term:mandate)`, `[Mapping](/mapping)`).
  A `term:` link is a glossary term: its text should match the term in `glossary.json`.

## Style

- Meaning over words: translate what the English means for a manager reading it, not word by word.
- Keep it as short as the English; headings and buttons especially.
- Same English term → same translation everywhere (see `glossary.json`).
- **Topology names stay English** (AK 2026-10-11): “Resource Topology”, “Delivery Topology”, “Adaptive Topology” (and the short forms Resource / Delivery / Adaptive) in Latin letters, never translated or transliterated.
- **Don't add brackets yourself:** on the first glossary term of each section the site shows the English term with your translation in brackets, e.g. “Mandate (Mandat)” (AK 2026-10-12).
- **Names that stay English:** besides the topologies, the MADE steps (Map, Assess, Design, Elevate), the four intelligences, “Org topologist” and the book-coined concepts whose `term` in `glossary.json` is English (Unpinning, Ferrari effect …). Translate only their definitions.

### Italian style
- Address the reader as **tu**. Plain modern Italian; Italian practitioners keep many English terms (Value stream, Output, Outcome, backlog).
- Headings and menu items short; the header tagline at most 30 characters.
- Same English term → same Italian (see `glossary.json`, e.g. Mandato, Progettazione organizzativa, Agente IA).
- **Keep the four intelligences in English:** Directing, Driving, Doing, Delivering (and “Directing Intelligence” etc.). They are core Org Topologies concepts shared by the global OT community.
- **Topology names stay English** (AK 2026-10-11): Resource Topology, Delivery Topology, Adaptive Topology (and the short forms).

## Checklist for a reviewed entry

1. Means the same as `en`; nothing added, nothing missing.
2. Uses the glossary terms.
3. Reads naturally to a native reader; would fit on a slide.
4. Formatting marks, placeholders and link targets unchanged.
5. `status` set to `reviewed`.

## How a change goes live

Commit to `main` or open a pull request. At the next site release the text is copied into the site and checked
(valid JSON, same formatting marks, links and placeholders as the English); an entry that breaks a rule stops the release
and is reported back. Then it is live at https://www.orgtopologies.com/it.

Questions or term discussions: Alexey Krivitsky.
