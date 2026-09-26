# Spritebell

Spritebell is a growing collection of personal Codex desktop companions. Each pet keeps its runnable package, visual previews, validation evidence, and generation provenance together.

## Pets

### Wonderbell

A chibi silver-haired AI agent operator with a bell ornament and a luminous constellation orb.

![Wonderbell animation overview](pets/wonderbell/previews/contact-sheet.png)

- Package: [`pet.json`](pets/wonderbell/pet.json) · [`spritesheet.webp`](pets/wonderbell/spritesheet.webp)
- Preview: [`16 look directions`](pets/wonderbell/previews/look-directions.png)
- Evidence: [`validation`](pets/wonderbell/qa/validation.json) · [`run summary`](pets/wonderbell/qa/run-summary.json)

### Suzu

A thoughtful agent-tanuki who scouts across borders, keeps evidence trails, and rings for human approval before irreversible leaps.

![Suzu animation overview](pets/suzu/previews/contact-sheet.png)

- Package: [`pet.json`](pets/suzu/pet.json) · [`spritesheet.webp`](pets/suzu/spritesheet.webp)
- Preview: [`16 look directions`](pets/suzu/previews/look-directions.png)
- Evidence: [`validation`](pets/suzu/qa/validation.json) · [`run summary`](pets/suzu/qa/run-summary.json)

### 菲比 (Feibi)

A gentle, radiant chibi companion with a lively spirit, known for greeting the workday with “菲比啾比”.

![Feibi animation overview](pets/feibi/previews/contact-sheet.png)

- Package: [`pet.json`](pets/feibi/pet.json) · [`spritesheet.webp`](pets/feibi/spritesheet.webp)
- Preview: [`16 look directions`](pets/feibi/previews/look-directions.png)
- Evidence: [`validation`](pets/feibi/qa/validation.json) · [`run summary`](pets/feibi/qa/run-summary.json)
- Creative direction: [`voice direction`](pets/feibi/provenance/voice-direction.md)

### 穂乃夏 (Honoka)

A cheerful travel companion inspired by 穂乃夏 from *anemoi*, ready to wave hello and set off together.

![Honoka animation overview](pets/honoka-anemoi/previews/contact-sheet.png)

- Package: [`pet.json`](pets/honoka-anemoi/pet.json) · [`spritesheet.webp`](pets/honoka-anemoi/spritesheet.webp)
- Preview: [`16 look directions`](pets/honoka-anemoi/previews/look-directions.png)
- Evidence: [`validation`](pets/honoka-anemoi/qa/validation.json) · [`run summary`](pets/honoka-anemoi/qa/run-summary.json)

### 朱比華 (Spica)

An unofficial fan-made companion inspired by Key's 辻倉朱比華 from *anemoi*: silver hair, a side bun, a pink coat, and a quietly determined gaze. [Official character reference](https://key.visualarts.gr.jp/anemoi/character.html).

![Spica animation overview](pets/spica-anemoi/previews/contact-sheet.png)

- Package: [`pet.json`](pets/spica-anemoi/pet.json) · [`spritesheet.webp`](pets/spica-anemoi/spritesheet.webp)
- Preview: [`16 look directions`](pets/spica-anemoi/previews/look-directions.png)
- Evidence: [`validation`](pets/spica-anemoi/qa/validation.json) · [`run summary`](pets/spica-anemoi/qa/run-summary.json) · [`direction QA`](pets/spica-anemoi/qa/direction-semantics.json)

### 陽彩 (Hiiro) — revision in progress

The current package is an outdated draft: it mistakenly depicts Key's 淡雪陽彩 with symmetrical twin tails. Her [official character art](https://key.visualarts.gr.jp/anemoi/character.html) shows an asymmetrical, side-tied sweep of long hair. A corrected companion is being prepared; please do not treat the linked draft as a faithful likeness.

- Archived draft: [`pet.json`](pets/hiiro-anemoi/pet.json) · [`spritesheet.webp`](pets/hiiro-anemoi/spritesheet.webp)
- Previous QA record: [`validation`](pets/hiiro-anemoi/qa/validation.json) · [`run summary`](pets/hiiro-anemoi/qa/run-summary.json)

## Install a pet

Copy one complete pet directory into `~/.codex/pets/<pet-id>/`. The two runtime files must remain beside each other:

```text
~/.codex/pets/<pet-id>/
├── pet.json
└── spritesheet.webp
```

The `previews/`, `qa/`, and `provenance/` directories are archive material and are not required at runtime.

## Repository layout

```text
pets/<pet-id>/
├── pet.json
├── spritesheet.webp
├── previews/
│   ├── contact-sheet.png
│   └── look-directions.png
├── qa/
│   ├── validation.json
│   └── run-summary.json
└── provenance/
    ├── pet-request.json
    └── voice-direction.md (when available)
```

Every current pet uses Sprite v2: an 8 × 11 atlas at `1536 × 2288`, with nine standard work-state rows and sixteen clockwise look directions.

> `run-summary.json`, `validation.json`, and `pet-request.json` keep creation-time path context using the public-safe placeholders `<LOCAL_HOME>` and `<LOCAL_TEMP>`. They are evidence records, not portable installation manifests.
