# Knowledge Base Schema

This repository follows the LLM Wiki pattern from `llm-wiki.md`.

## Layer Map

- `raw/` holds immutable source material. Add new sources here, but do not edit them after ingest.
- `wiki/` holds the maintained knowledge base. This is the LLM-owned synthesis layer.
- `outputs/` holds derived deliverables such as slides, reports, and figures.

## Wiki Rules

- Read `wiki/index.md` first when answering a question or starting an ingest pass.
- Update relevant wiki pages when new sources change the current synthesis.
- Append every ingest, query, or lint pass to `wiki/log.md`.
- Keep page names lowercase and kebab-case.
- Prefer concise markdown pages with clear links to related topics.

## Standard Workflow

### Ingest

1. Read the new source from `raw/`.
2. Extract the key claims, entities, concepts, methods, and open questions.
3. Update the relevant pages in `wiki/`.
4. Refresh `wiki/index.md` so the new or changed pages are discoverable.
5. Append an entry to `wiki/log.md`.

### Query

1. Read `wiki/index.md` to locate the most relevant pages.
2. Read the pages that matter, not the entire repository.
3. Synthesize from the wiki first, then fall back to raw sources if needed.
4. File useful answers back into the wiki when they add lasting value.

### Lint

1. Look for contradictions between pages.
2. Look for missing cross-references and orphan pages.
3. Look for stale claims that newer sources supersede.
4. Propose new pages when an important topic has no dedicated page.

## Page Conventions

- Use markdown.
- Keep an opening summary near the top.
- Add a short `Related` section when useful.
- Link to other wiki pages whenever a connection matters.
- Include source links or provenance notes when a page is based on raw material.

## Index And Log

- `wiki/index.md` is the content-oriented catalog.
- `wiki/log.md` is the chronological record.
- Keep both current as the wiki grows.
