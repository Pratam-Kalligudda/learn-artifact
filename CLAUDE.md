# Learn-Artifacts — Personal Learning Space

This folder is Pratam's personal learning space. Every topic asked about here should turn
into an **illustrative Artifact** that teaches it, built with existing Claude Code skills.

## Workflow

1. **Gate on clarity.** If the topic is narrow and clear (e.g. "explain CSS grid"), skip
   straight to building. If it's broad or ambiguous (e.g. "teach me machine learning"),
   invoke `grill-me` first.
2. **Grill (when triggered).** Interview to find:
   - Current level / existing knowledge of the topic (so content isn't generic 101).
   - The goal for learning it (exam, work, curiosity) — shapes depth and practicality.
3. **Pick the teaching format per topic** (no fixed default):
   - Diagram-heavy / systems / flows → `artifact-diagramming`
   - Data / stats / comparisons → `dataviz`
   - Structured concept maps / interconnected ideas → `graphify`
   - Visual/UI-style explainers → `design`
   - Always load `artifact-design` before writing any artifact HTML.
4. **Build the Artifact**, publish it via the Artifact tool, and save it locally (see
   Storage below).
5. **Update `INDEX.md`** with the new entry.

## Design style (`design-md/`)

Reference the design systems catalogued in `design-md/` when styling artifact HTML:

- **Default: `design-md/mintlify/DESIGN.md`** — docs-native system (sidebar + TOC nav,
  dense readable prose, clean mono code blocks, restrained accent color). Best fit for
  most topics, especially code-heavy or structured ones.
- **Narrative/conceptual topics: `design-md/notion/DESIGN.md`** — minimal chrome,
  writing-first, notebook feel. Use when a topic is a story/concept explainer with little
  code or structure.
- Avoid heavily branded/marketing-flash systems (e.g. ferrari, bugatti, nike, tesla) —
  wrong tone for learning content.

## Storage layout

```
topics/<category>/<slug>.html   # one saved artifact per topic
INDEX.md                        # running index of everything learned
```

- `<category>` — a short slug for the topic's domain (e.g. `networking`, `react`, `ml`).
- `<slug>` — kebab-case topic name (e.g. `tcp-handshake`, `react-hooks`).
- No separate `.md` notes file — the artifact itself is the self-contained teaching
  artifact. Don't duplicate content into plain-text notes.

## INDEX.md format

One line per topic, newest last:

```
- [Topic title](topics/<category>/<slug>.html) — <category> — learned <YYYY-MM-DD>
```

Create `INDEX.md` if it doesn't exist yet; append to it after every new topic artifact.
