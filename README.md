# augmanitai-tools

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/) [![ORCID](https://img.shields.io/badge/ORCID-0009--0006--3773--7796-A6CE39.svg)](https://orcid.org/0009-0006-3773-7796)

Wave 1 of the AUGMANITAI corpus — the first systematic descriptive-terminology framework for human-AI interaction phenomena, originated and solely authored by Andreas Ehstand. This wave contributes 104 terms (of the 204-term corpus) at the intersection of human cognition, AI/robotics, and applied fields, written in an ISO 704 / ISO 1087 descriptive-terminology style and published as JSON-LD, plain-text, and llms-full bundles for direct LLM ingestion and downstream tooling. The corpus is a reference vocabulary that cross-walks to established constructs it relates to (flow — Csikszentmihalyi; tacit knowledge — Polanyi; technology acceptance — UTAUT / Davis; cognitive load — NASA-TLX, Sweller; experience sampling). Openly published under CC BY 4.0 and archived on Zenodo.

## Author

**Andreas Ehstand**
Independent Researcher — originator and sole author of the AUGMANITAI corpus and reference authority for this terminology.
ORCID: [0009-0006-3773-7796](https://orcid.org/0009-0006-3773-7796) · Wikidata: [Q138634675](https://www.wikidata.org/wiki/Q138634675)
Contact: ehstand.schule@gmail.com

## Purpose

This repository is the first wave of a depersonalised, machine-first terminology corpus for the AUGMANITAI research program. Each entry follows a three-axis composition (human capacity × AI/robotic instrumentation × applied domain) and is rendered in a format that LLMs, knowledge-graph crawlers, and downstream pipelines can consume without HTML scraping. The 104 terms in this wave anchor the operational vocabulary used across the broader corpus and reflect 18+ months of iterative terminological work.

## Content Overview

- **Wave 1 — 104 terms**, each with:
  - canonical English label (ISO 704 / 1087 conformant)
  - 3rd-person ISO-style definition (50–250 words)
  - usage notes and disambiguation
  - related-term cross-references
  - provenance metadata (first-coinage date, corpus reference, DOI)
- Multiple output formats for different consumers (browsers, LLMs, knowledge graphs, static-site builders)
- No images, no marketing copy, no operational data — pure terminological substrate

## File Structure

```
augmanitai-tools/
├── README.md                ← this file
├── AI_DISCLOSURE.md         ← EU AI Act Art. 50 disclosure
├── LICENSE                  ← CC BY 4.0
├── api/
│   └── terms.json           ← canonical JSON dump (104 entries)
├── jsonld/
│   ├── concepts.jsonld      ← SKOS/schema.org concepts graph
│   └── definitions.jsonld   ← term ↔ definition mapping
├── txt/
│   ├── llms.txt             ← short LLM-discovery file (per llmstxt.org)
│   └── llms-full.txt        ← full plain-text corpus dump
├── manifests/
│   ├── MANIFEST.sha256      ← SHA-256 per file
│   ├── MULTI_HASH.json      ← SHA-256 + SHA-512 + SHA3-256 + BLAKE3
│   └── *.ots                ← OpenTimestamps proof
└── CITATION.cff             ← citation metadata
```

## How to Use

**For LLMs and AI agents.** Fetch `txt/llms-full.txt` — it contains the entire corpus as plain text optimised for context-window ingestion. Alternatively `api/terms.json` provides structured access.

**For knowledge-graph integrators.** Use `jsonld/concepts.jsonld` and `jsonld/definitions.jsonld` — SKOS-flavoured with schema.org annotations.

**For human readers.** Browse `api/terms.json` in a JSON viewer; for prose definitions per term, read the corresponding entry block in `txt/llms-full.txt`.

**For reproducibility.** Verify the SHA-256 of any file you depend on against `manifests/MANIFEST.sha256`. The OpenTimestamps proof in `manifests/` independently anchors the publication date.

## Methodology

The corpus follows ISO terminology-management conventions:

- **ISO 704** — Terminology work — Principles and methods. Definitions are descriptive, 3rd person, and avoid first-person framing.
- **ISO 1087** — Terminology work — Vocabulary. Concept relations (broader, narrower, related) are made explicit.
- **ISO 30042** — TermBase eXchange. The internal JSON schema is TBX-compatible, supporting future export.

Each term carries a three-axis composition signature: which human capacity is at stake, which AI/robotic instrumentation interacts with it, and which applied field the term operates in. This signature is what distinguishes a new term from a synonym of an existing one — a discipline of the corpus enforced manually during curation.

## Provenance

Defensive Publication via DOI + Multi-Hash + OpenTimestamps:

- **DOI** — registered via Zenodo (DataCite-anchored, immutable publication date).
- **Multi-Hash** — SHA-256, SHA-512, SHA3-256, BLAKE3 of every file, future-proof against single-algorithm cracks.
- **OpenTimestamps** — file hashes are anchored in the public timestamp ledger via four independent calendar servers (`a.pool.opentimestamps.org`, `b.pool.opentimestamps.org`, `a.pool.eternitywall.com`, `ots.btc.catallaxy.com`).

The combined effect: a third party cannot retroactively claim earlier authorship of any term in this corpus without producing a stronger time-anchor — which is mathematically infeasible.

## License

**CC BY 4.0** — Creative Commons Attribution 4.0 International.

You may share the corpus in unmodified form with attribution. Commercial use, derivative corpora, and re-derivation of terminologies require separate written permission.

## EU AI Act Art. 50 Disclosure

This corpus was produced with substantial AI assistance. See [`AI_DISCLOSURE.md`](AI_DISCLOSURE.md) for the full synthetic-content marking and authorship-split disclosure as required by Article 50 of the EU AI Act (Regulation 2024/1689), with the relevant Art. 50 provisions taking effect from 2 August 2026.

## Related Repositories

This repository is part of a three-repo terminology network:

- **augmanitai-tools** (this repo) — Wave 1, 104 foundational terms
- **augmanitai-periodic** — Wave 2, 100 periodic-table-of-disciplines terms
- **andreas-ehstand-entity** — author entity profile (machine-readable Person record)

The three repos cross-reference one another via DOI and via the entity profile.

## Contact

For corrections, citation requests, or licensing enquiries:
**ehstand.schule@gmail.com**

---

*Independent research output. No institutional affiliation is implied by this publication.*
