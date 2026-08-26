# Spritebell Agent Rules

Spritebell archives Codex-compatible desktop pets. Keep every pet self-contained under `pets/<pet-id>/`.

## Required package

- `pet.json` and `spritesheet.webp` are the runnable package and must be committed together.
- New pets must use `spriteVersionNumber: 2` and a validated `1536x2288` spritesheet.
- Preserve the pet id across the directory name, `pet.json`, and installation path.

## Archive layout

- Put user-facing contact sheets and direction previews in `previews/`.
- Put deterministic validation and final run summaries in `qa/`.
- Put the final generation request or equivalent source record in `provenance/`.
- Do not commit generated row strips, extracted frames, layout guides, temporary PNGs, or tool caches.

## Changes

- Preserve existing pets when adding a new one.
- Update the root `README.md` catalog for every added, renamed, or materially revised pet.
- Verify JSON syntax, `pet.json` package paths, atlas dimensions, and a scoped Git diff before committing.
