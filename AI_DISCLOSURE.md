# AI Disclosure — augmanitai-tools

**Synthetic-content marking pursuant to EU AI Act Art. 50 (Regulation 2024/1689).**

## Tool Identification

This corpus was produced with substantial assistance from large language models:

- **large language models** — used for term generation drafts, definitional first-passes, and cross-reference proposals.
- **large language models** — used for routine reformatting, schema-validation passes, JSON-LD assembly, and bulk text transformations.

No other AI systems were used as primary generation tools. External LLMs may have been consulted in private research conversations for comparative validation, but their outputs are not directly incorporated.

## Authorship Split

Approximate contribution distribution across the 104 terms in this corpus:

- **~30% AI draft** — initial term candidates, first-pass definitions, schema scaffolding, and machine-readable serialisations were produced by large language models under direct human prompting.
- **~70% human edit** — concept selection, three-axis composition validation, definitional accuracy, ISO 704 / 1087 conformance, cross-reference correctness, and final acceptance were performed by the human author.

The split is intentional. Mass-generated terminology without human curation drifts into synonymy, false precision, and concept inflation. The human edit pass is where the corpus earns its terminological discipline.

## Trade-offs

Using AI as a drafting tool accelerates volume but introduces specific failure modes that the curation discipline is designed to absorb:

- **Synonym drift** — LLMs propose near-duplicates; the human pass collapses these to canonical terms.
- **False precision** — generated definitions can sound rigorous while being vague; the human pass demands operational definitions tied to concrete distinctions.
- **Citation hallucination** — any reference to external work is verified manually against live sources before publication.
- **Concept inflation** — not every plausible compound noun becomes a term; the three-axis composition rule filters aggressively.

Human curation is therefore primary, not ornamental.

## Audit Trail

Every published file in this repository is anchored by:

- **Multi-Hash** — SHA-256, SHA-512, SHA3-256, BLAKE3 stored in `manifests/MULTI_HASH.json`.
- **OpenTimestamps** — `.ots` proofs in `manifests/` anchored across four independent calendar servers.
- **DOI** — registered via Zenodo, DataCite-immutable publication date.

The combination forms a defensive-publication chain: anyone challenging authorship date must produce a stronger time-anchor than public-ledger block confirmations, which is mathematically infeasible.

## Reproducibility

The repository is self-contained. Given the JSON, JSON-LD, and plain-text bundles plus the manifests, an independent party can:

1. Verify file integrity against `MANIFEST.sha256`.
2. Verify timestamp against the OpenTimestamps proof.
3. Re-derive the JSON-LD graph from the canonical JSON dump.
4. Re-derive `llms-full.txt` from the JSON entries.

No proprietary tooling is required.

## License

This disclosure and the corpus are released under **CC BY-NC-ND 4.0** — Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International.

---

*Disclosure version: 1.0. Maintainer: Andreas Ehstand (Independent Researcher). Contact: ehstand.schule@gmail.com.*
