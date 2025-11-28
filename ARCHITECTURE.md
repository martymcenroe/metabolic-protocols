# Metabolic Protocols Architecture

## 1\. System Overview

The `metabolic-protocols` repository serves as the definitive source of truth for the Principal Architect's bio-hacking and metabolic optimization program. It treats nutrition and health interventions as "Infrastructure as Code."

## 2\. Design Principles

  * **Zero-Carb Constraint:** All data entities must adhere to strict zero-carb/ketogenic parameters unless explicitly tagged as `legacy` or `family`.
  * **Data as Code:** Recipes and protocols are stored as structured data (Markdown + YAML Frontmatter), not unstructured prose.
  * **Reproducibility:** Protocols must be deterministic. Instructions should include quantitative metrics (temperature, time, weight) rather than qualitative descriptors.

## 3\. Data Schema

All protocol files reside in `src/protocols/` and adhere to the following Frontmatter schema:

```yaml
---
title: "Protocol Name"
tags: ["zero-carb", "recovery", "high-fat"]
macros:
  carbs: 0g
  fat: "high"
  protein: "moderate"
prep_time: "ISO8601 Duration (e.g., PT15M)"
cook_time: "ISO8601 Duration (e.g., PT18H)"
---
```

## 4\. Technology Stack

  * **Language:** Python 3.11+
  * **Dependency Management:** Poetry
  * **Validation:** Pydantic (Planned)
  * **CI/CD:** GitHub Actions (Planned) for automated macro auditing.