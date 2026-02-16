# Analysis of the MARC Pilot Project Final Report

**Source:** *The MARC Pilot Project: Final Report* by Henriette D. Avram, Library of Congress, 1968 (ED 029 663)

**Purpose:** Evaluate how this document relates to the hypothesis that MARC's 3-digit field tags originated from punch card sequence numbering conventions used in pre-MARC library cataloging.

---

## Key Finding: MARC I Used 2-Digit Tags, Not 3-Digit

The MARC pilot system (MARC I) used **two-character tags** — 10, 20, 30, 40, 50, 60, 70, 80, 90 — not the familiar 3-digit tags like 100, 245, 610. The 3-digit tags came later with **MARC II**.

### MARC I Tag Table

| Tag | Description |
|-----|-------------|
| 10  | Main Entry |
| 15  | Conventional or Filing Title |
| 20  | Title Statement |
| 25  | Edition Statement |
| 30  | Imprint Statement |
| 40  | Collation Statement |
| 50  | Series Note (traced same) |
| 51  | Series Note (traced differently/untraced) |
| 60  | Notes |
| 70  | Subject Tracing |
| 71  | Personal Author Tracing |
| 72  | Corporate Author Tracing |
| 73  | Uniform Tracing |
| 74  | Title Tracing |
| 75  | Series Tracing |
| 80  | Copy Statement |
| 83  | National Bibliography Number |
| 90  | Library of Congress Call Number |
| 92  | Dewey Decimal Classification Number |
| 94  | Library of Congress Catalog Card Number Suffix |

These are sequential multiples of 5 and 10, with subtypes filling in gaps (71–75 for different tracing types, 92/94 for classification numbers). A third tag character was optional and alphanumeric (e.g., 72B for Government Body, 72C for Society).

### MARC II Introduced 3-Digit Tags with an Explicit Design Rationale

The report documents the MARC II tagging structure as a deliberate design:

> "In the design of MARC II, the tagging structure was based on assigning the primary digit a functional meaning and the secondary digits a 'type of name' meaning. For example, the tag for a corporate name subject entry is 610. The first digit (in this case '6') describes the function of the name, i.e., it serves as a subject entry. The second digit (in this case '1') indicates that the name is a corporate name."

The MARC II tag matrix:

| Function         | Personal (x00) | Corporate (x10) | Uniform Title (x30) | Title (x40/x45) |
|------------------|-----------------|------------------|----------------------|------------------|
| Main Entry (1xx) | 100             | 110              | 130                  | 245              |
| Series Note (4xx)| 400             | 410              | —                    | 440              |
| Subject (6xx)    | 600             | 610              | 630                  | —                |
| Added Entry (7xx)| 700             | 710              | 730                  | 740              |
| Series Tracing (8xx) | 800         | 810              | —                    | 840              |

---

## Evidence Relevant to the Hypothesis

### Connections That Support Further Investigation

1. **Yale had pre-existing automation before MARC.** The report confirms that LC "would draw heavily on the experience of the National Library of Medicine, University of Toronto, Florida Atlantic University, Yale University, and other agencies that already had projects underway." Yale operated the Yale Bibliographic System (YBS) and the CHY6 program, which predated the MARC Pilot Project by at least a year.

2. **80-column punch cards were widespread in library cataloging.** Indiana University was "key-punching and verifying of the edited order and cataloging information into 80-column tabulating cards." Nassau County Library was keypunching bibliographic data into Univac cards. King County Library in Washington had been producing catalogs with "IBM unit record equipment" since 1951.

3. **MARC I tags follow the traditional catalog card order.** The sequence 10 (main entry), 20 (title), 30 (imprint), 40 (collation), 50–51 (series), 60 (notes), 70–75 (tracings), 80 (copy), 90–94 (call numbers) mirrors the physical order of elements on a traditional catalog card — the same order seen on the Yale punch cards from 1965.

4. **The Yale punch card numbers map suggestively to MARC I tags.** The Yale punch cards use sequence numbers A100, A200, A400, A710, A730, A900 in columns 67–71. Dividing by 10 yields 10, 20, 40, 71, 73, 90 — which are MARC I tags for main entry, title, collation, personal author tracing, uniform tracing, and LC call number respectively.

5. **Nassau County assigned "arbitrary" item numbers to punch card decks.** This confirms that libraries were independently developing numbering conventions for punch card-based cataloging before MARC standardized the practice.

### Evidence That Complicates the Hypothesis

1. **MARC deliberately chose paper tape over punch cards.** The report states: "A survey of libraries in various stages of automation indicated that punched paper tape was more efficient for the processing of variable length bibliographic records than punched cards. The inconvenience of the limitation of the 80-column card and the necessity of linking one card to another by a unique number for field and record seemed to compensate for the added complexity of correction procedures with the use of paper tape."

2. **MARC II 3-digit tags have an explicit functional design rationale.** The first digit encodes function, the second encodes type of name. This is a documented, intentional system — not an inheritance from punch card conventions.

3. **No direct mention of punch card sequence numbers as a source.** The report contains no reference to columns 67–71, sequence numbers on punch cards, or the A100/A200 numbering pattern as inspiration for MARC tags.

4. **The MARC I format was shaped by IBM System/360 constraints.** The report notes: "The MARC I format was shaped by many constraints... its design was influenced by the emphasis of the project on distribution of LC cataloging information" and was "structured so as to lend itself readily to ease in programming on an IBM System/360 Model 30 with 16K core memory."

---

## The Missing Link: ISS Planning Memorandum No. 3

The report points to the key originating document for the MARC format:

> *A Proposed Format for a Standardized Machine-Readable Catalog Record* (ISS Planning Memorandum No. 3), by Henriette D. Avram, Ruth S. Freitag, and Kay D. Guiles, June 1965.

This is where the first tag assignments were made. The report also references the preceding **Inforonics study** (1964), *The Recording of Library of Congress Bibliographical Data in Machine Form*, which studied methods of converting LC catalog card information to machine-readable form.

Neither document is included in the report. **ISS Planning Memorandum No. 3 is the document most likely to contain the original rationale for the tag numbering scheme** — whether it was influenced by existing punch card conventions or designed independently.

---

## Other Notable Details

- **Input procedures used a Dura Mach 10 typewriter** that produced both typed copy and punched paper tape. Tags had to be entered in numerical order due to program specifications.
- **MARC I had no directory** — variable fields were simply concatenated sequentially, each prefixed by a 3-character length and a tag. MARC II introduced a consolidated directory with tag, field length, and starting character position.
- **The Inforonics study (1964)** preceded and informed MARC. It was commissioned by the Council on Library Resources and submitted November 23, 1964.
- **Yale's Frederick G. Kilgour** (who later founded OCLC) was among the Yale participants. Yale had to build a MATE program to translate MARC records into their pre-existing YBS format, confirming that Yale's local system used a different data structure than MARC.

---

## Conclusion

The MARC Pilot Project report does not confirm or deny the hypothesis directly. It establishes that:

1. The familiar 3-digit MARC tags (100, 245, etc.) are a **MARC II innovation** with documented functional design rationale.
2. The earlier MARC I 2-digit tags (10, 20, 30...) have **no documented rationale** in this report.
3. Yale and other libraries were using punch card-based cataloging systems **before MARC**, and LC drew on their experience.
4. The numerical correspondence between Yale punch card sequence numbers (A100, A200...) and MARC I tags (10, 20...) is suggestive but unconfirmed.

The trail leads to **ISS Planning Memorandum No. 3 (June 1965)** as the next document to investigate for the original tag numbering rationale.
