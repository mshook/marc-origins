# CLAUDE.md

## Project Overview

This is a **historical research repository** investigating the origins of the MARC (Machine-Readable Cataloging) library catalog format. The central hypothesis explores whether MARC's 3-digit field tags originated from IBM punch card sequence numbering conventions used in library cataloging before MARC was formalized.

This is **not a software project** — it contains no source code, build system, or tests. It is a collection of research notes, reference documents, and primary source materials.

## Repository Structure

```
marc-origins/
├── README.md                              # Brief project description
├── LICENSE                                # MIT License (mshook, 2026)
├── CLAUDE.md                              # This file
├── MarcOriginInPunchedCards.tid           # Primary research notes (TiddlyWiki format)
├── MARC_standards.pdf                     # Wikipedia article on MARC standards
├── View of MARC II and COBOL.pdf          # Historical MARC II reference document
├── marc pilot project ed029663[1].pdf     # Original MARC pilot project documentation
└── Screenshot 2026-02-15 9.58.56 PM.png  # Project screenshot
```

## Key Files

- **`MarcOriginInPunchedCards.tid`** — The core research document. Contains the hypothesis, evidence from Yale library punch cards (1965), punch card ASCII reproductions, and references to Henriette Avram's role in creating MARC. Written in TiddlyWiki markup format (`.tid`).
- **`MARC_standards.pdf`** — Background reference on MARC standards.
- **`View of MARC II and COBOL.pdf`** — Historical document on MARC II and its relationship to COBOL.
- **`marc pilot project ed029663[1].pdf`** — Documentation from the original MARC pilot project.

## Research Context

- **MARC** (Machine-Readable Cataloging) is a standard for representing bibliographic information in machine-readable form, created by Henriette Avram at the Library of Congress in the 1960s.
- The hypothesis here is that MARC's 3-digit tags (e.g., 100 for author, 245 for title) may derive from the tradition of using columns 67–71 of 80-column IBM punch cards as sequence numbers in pre-MARC library cataloging systems.
- Evidence includes Yale library punch cards from 1965 showing sequence numbers in those columns that resemble MARC field tag patterns.

## File Format Notes

- **`.tid` files** are TiddlyWiki tiddler files. They have a metadata header (created, creator, modified, modifier, tags, title, type) followed by content in TiddlyWiki markup. `!!` and `!!!` denote headings; `*` denotes list items; triple backticks denote code blocks.
- **PDF files** are reference documents and should not be modified.

## Conventions for AI Assistants

- Preserve the existing flat directory structure — do not reorganize files into subdirectories.
- The `.tid` file uses TiddlyWiki markup conventions; maintain this format when editing.
- File names may contain spaces and special characters (e.g., `marc pilot project ed029663[1].pdf`); handle these carefully in shell commands by quoting paths.
- This repository has no build steps, linters, formatters, or test suites to run.
- When adding new research content, follow the existing pattern: primary notes in `.tid` format, reference documents as PDFs.
