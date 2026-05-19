# ToxCastLite Project Website

This repository contains the static project website for **ToxCastLite: A portable semantic evidence graph linking in vitro bioactivity, in vivo toxicity, and exposure-use context**.

**Project website:** <https://toxcast-lite.github.io/>  
**Preprint DOI:** <https://www.biorxiv.org/content/10.64898/2026.05.16.724895v1>  
**Status:** public project landing page for a research prototype.

## Purpose of this repository

This repository is **not** the software repository and does **not** distribute the ToxCastLite evidence stores.

It contains only the static website used to communicate the project concept, motivation, preprint, demo material, references, and contact information.

The website is designed for:

- regulatory and agency-facing audiences,
- toxicologists and risk assessors,
- computational toxicology researchers,
- collaborators and reviewers,
- users interested in local, portable, and auditable evidence workflows.

## What ToxCastLite is

ToxCastLite is a portable evidence-access framework for integrated toxicology data mining.

The project combines assay-scoped SQLite evidence stores with a compact RDF layer for semantic discovery. Dense numerical evidence remains in SQLite, while query-relevant entities are exposed through RDF and queried through a SPARQL endpoint in the demonstrated prototype.

In the current preprint, ToxCastLite links three evidence layers:

- **ToxCast/invitrodb** in vitro bioactivity and concentration-response evidence,
- **ToxRefDB** in vivo apical toxicity evidence,
- **CPDat** product-use, functional-use, and list-presence context.

The layers are connected through chemical identifiers such as DSSTox Substance Identifiers. This makes it possible to ask evidence-oriented questions across NAM bioactivity, curated in vivo evidence, and exposure-relevant use context without directly navigating the original MySQL, PostgreSQL, SQLite, RDF, or SPARQL structures.

## Main message

ToxCastLite provides **portable semantic access to toxicology evidence stores**.

The key idea is to separate two tasks:

1. **Efficient local storage of dense evidence**
   - SQLite stores concentration-response rows, model outputs, quality flags, CPDat records, ToxRefDB study evidence, and source-level identifiers.

2. **Semantic discovery across linked evidence**
   - RDF exposes chemicals, assays, endpoints, model results, potency fields, quality flags, product-use context, point-of-departure records, effect summaries, and observation summaries as queryable graph entities.

This hybrid design supports local evidence retrieval, prioritization, drill-down, and expert review while keeping interpretation under human control.

## Website structure

The website is intentionally simple and public-facing.

1. **Full-screen demo video**
   - A short visual demonstration introduces the workflow before the user reads the text.

2. **Project summary**
   - Briefly explains what ToxCastLite is and how it connects SQLite evidence stores with semantic access.

3. **Why it matters**
   - Highlights the core value:
     - portable evidence stores,
     - semantic discovery,
     - CPDat use-context integration,
     - ToxRefDB in vivo evidence integration,
     - drill-down to source-level records.

4. **Research prototype scope**
   - Makes clear that the website presents a research prototype and project concept, not a hosted regulatory decision system.

5. **Local, auditable workflows**
   - Explains the intended use context for scientific and regulatory review, including traceability from graph-level results back to SQLite records.

6. **Preprint and references**
   - Links the project page to the public preprint and the scientific and technical references behind the work.

7. **Contact and attribution**
   - Provides institutional and project-lead contact links.

## Important scope note

This repository contains only the static website.

It does **not** contain:

- the ToxCastLite software pipeline,
- MySQL-to-SQLite builder scripts,
- RDF projection scripts,
- generated SQLite databases,
- RDF dumps,
- a GraphDB instance,
- CPDat, ToxCast, or ToxRefDB source data,
- a deployed Streamlit application,
- a deployed LLM backend.

For software, data-builder workflows, RDF projection scripts, prototype access, or collaboration requests, please use the contact links below.

## GraphDB and replaceable infrastructure

The preprint demonstrates a prototype implementation in which **GraphDB** is used as the RDF/SPARQL engine for semantic discovery.

GraphDB is third-party software and is **not** part of this repository. This repository does not redistribute GraphDB binaries, containers, licenses, configurations, or commercial deployments.

ToxCastLite is conceptually based on standard RDF and SPARQL access patterns. In principle, GraphDB can be replaced by another suitable RDF store or SPARQL endpoint, subject to engineering, performance, and deployment requirements.

Users and institutions are responsible for ensuring that any third-party software they use, including GraphDB or alternative RDF stores, is used under the appropriate license terms.

## Data sources and responsibility

ToxCastLite is built from publicly available toxicology data resources, including ToxCast/invitrodb, ToxRefDB, and CPDat.

The project generates derived SQLite evidence stores and RDF projections to support semantic access, evidence linking, prioritization, and drill-down. It does not modify the underlying scientific content of the source databases.

The website and preprint should not be interpreted as providing:

- an automated hazard assessment,
- an automated risk assessment,
- a regulatory decision,
- a warranty of completeness or accuracy of the source data,
- a claim that CPDat product-use context represents measured exposure,
- a claim that absence of evidence in the graph means evidence of absence.

Final toxicological or regulatory interpretation remains the responsibility of qualified experts.

## Repository layout

```text
toxcast-lite.github.io/
├── index.html
├── README.md
└── assets/
    └── toxcastlite-demo.mp4
```

## Contact links

The website currently links to:

- Project website: <https://toxcast-lite.github.io/>
- DNTOX GmbH: <https://dntox.de/#>
- IUF – Leibniz Research Institute for Environmental Medicine: <https://iuf-duesseldorf.de>
- Project lead: <https://arifdoenmez.github.io/>

## Preprint citation

Dönmez, A., Nosov, O., Heck, K., Mosig, A., Fritsche, E., & Koch, K. (2026). **ToxCastLite: A portable semantic evidence graph linking in vitro bioactivity, in vivo toxicity, and exposure-use context.** Preprint. <https://doi.org/10.64898/2026.05.16.724895>

## References shown on the website

The landing page may reference the following scientific and technical background sources:

1. Dix et al. (2007), ToxCast program.
2. Richard et al. (2016), ToxCast chemical landscape.
3. EPA ToxCast database / invitrodb version 4.3.
4. EPA ToxRefDB v3.0.
5. Feshuk et al. (2023), ToxRefDB v2.1 update.
6. Handa et al. (2025), CPDat v4.0.
7. Sheffield et al. (2022), tcplfit2.
8. Angles and Gutierrez (2008), graph database models.

These references connect the project website to the scientific and technical background of the preprint. They should not be read as claims that third-party datasets or software are redistributed by this repository.
