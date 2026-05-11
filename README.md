# ToxCastLite Project Website

This repository contains the static website for **ToxCastLite: Portable Semantic Access to ToxCast Evidence Stores**.

The website is intended as a short public-facing project page. It presents a 30-second demo video as the main entry point, followed by a concise summary of the ToxCastLite concept, its motivation, key features, references, and contact information.

## Purpose of the website

The website is not the software repository itself. It is the project landing page for communicating what ToxCastLite is and why it matters.

It is designed for:

- regulatory and agency-facing audiences,
- toxicologists and risk assessors,
- collaborators and reviewers,
- users interested in local, portable toxicology evidence workflows.

## Main message

ToxCastLite provides portable semantic access to ToxCast evidence stores.

The project combines:

- assay-scoped SQLite evidence stores,
- RDF/GraphDB-based semantic discovery,
- CPDat product-use and functional-use context,
- drill-down access to concentration–response evidence,
- and local, auditable workflows for regulatory and scientific users.

## Website structure

The website is intentionally simple:

1. **Full-screen demo video**
   - A short 30-second visual demonstration appears on the first screen.
   - The video should communicate the workflow without requiring the user to read first.

2. **Short project summary**
   - Explains what ToxCastLite is.
   - Emphasizes portable SQLite evidence stores and RDF/GraphDB semantic access.

3. **Why it matters**
   - Four short cards summarize the core value:
     - portable evidence stores,
     - semantic access,
     - CPDat context,
     - evidence drill-down.

4. **Local, auditable workflows**
   - Explains the intended regulatory/scientific use context.
   - Includes links to DNTOX and references.

5. **References**
   - Lists the key scientific and technical references behind the project.

6. **Footer attribution**
   - Quietly credits the project lead and institutional context.

## File layout

Recommended repository layout:

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

## References shown on the website

The landing page currently references:

1. Dix et al. (2007), ToxCast program.
2. Richard et al. (2016), ToxCast chemical landscape.
3. EPA ToxCast database (invitrodb) version 4.3 dataset.
4. Handa et al. (2025), CPDat v4.0.
5. Sheffield et al. (2022), tcplfit2.
6. Angles and Gutierrez (2008), graph database models.

These references are included to connect the website text to the scientific and technical background of the project.

## Notes

This repository is only the static project website. For the software, data builders, RDF projection scripts, and prototype interface use the contact links.
