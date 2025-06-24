# Academic Articles Accessibility Dataset

This repository contains the **final** set of documents classified by accessibility and organized as follows:

```text
/class0   → inaccessible PDFs  
/class1   → accessible PDFs
```

Labelling follows the checkpoints of the **Matterhorn Protocol** as evaluated by the **PDF Accessibility Checker (PAC)**.

---

## Table of Contents
1. [Accessibility Context in PDF](#accessibility-context-in-pdf)  
2. [Matterhorn Protocol](#matterhorn-protocol)  
3. [PDF Accessibility Checker (PAC)](#pdf-accessibility-checker-pac)  
4. [References](#references)

---

## Accessibility Context in PDF

Digital accessibility requires that content be usable by everyone, including people who rely on assistive technologies.  
Scientific articles in **PDF** format often lack semantic tagging, header navigation and language metadata, which hampers their interpretation by screen readers.  
Although the Brazilian Inclusion Act (Law 13.146/2015) mandates equal access in higher education, recent studies reveal a high prevalence of structural issues in institutional repositories and commercial publishers.

---

## Matterhorn Protocol

The **Matterhorn Protocol** (PDF Association, 2013 / rev. 2021) converts the **PDF/UA (ISO 14289‑1)** standard into *136 failure conditions*:

| Block                | Checkpoint example | Matterhorn IDs |
|----------------------|--------------------|----------------|
| Basic Requirements   | `/Tagged` flag     | 01–12, 18, 20–22, 30–31 |
| Logical Structure    | heading hierarchy  | 09, 13–19, 27–28 |
| Metadata & Settings  | global language    | 03–08, 23–26, 29 |

Within this *dataset*, failures in **PDF Syntax** automatically label the document as **inaccessible**, regardless of other checks.

---

## PDF Accessibility Checker (PAC)

[**PAC 2024**](https://www.axes4.com/) implements most Matterhorn checkpoints and produces three main outputs:

* **Summary** — passed, warning or failed  
* **Technical report** — list of errors, their locations and fix suggestions  
* **Tag tree** — visualisation of the document’s logical structure  

The results are grouped into:

| PAC block            | Items verified                                                                |
|----------------------|-------------------------------------------------------------------------------|
| Basic Requirements   | PDF Syntax, Fonts, Content, Embedded Files, Natural Language                  |
| Logical Structure    | Structure Elements, Structure Tree, Role Mapping, Alternative Descriptions    |
| Metadata & Settings  | Metadata, Document Settings                                                   |

Critical failures in **PDF Syntax** (e.g., missing `/Tagged` flag) halt the audit and classify the PDF as inaccessible.

---

## References

- **Adobe.** *PDF Accessibility Overview*, 2023.  
- **axes4.** *PAC 2024 – PDF Accessibility Checker*, 2024.  
- **Brazil.** Law 13.146 / 2015 (*Brazilian Inclusion Act*).  
- **Darvishy F. et al.** “Accessibility in Swiss Repositories”, 2023.  
- **Guimarães J.** “PDF Accessibility in Academic Publishing”, 2019.  
- **PDF Association.** *Matterhorn Protocol* v1.1, 2021.  
- **Pierres E.** “Semantic Tags in University Repositories”, 2024.  

*All texts are available in open access.*
