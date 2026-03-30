# Avicenna ESM Compliance Monitoring Tool

A beginner-friendly R Markdown template for monitoring **Experience Sampling Method (ESM) compliance** in studies that use [Avicenna](https://avicennaresearch.com/) to collect data.

**Author:** Robin Achterhof — [achterhof@essb.eur.nl](mailto:achterhof@essb.eur.nl)

---

## What it does

Knit the `.Rmd` file at any point during your study to get an HTML report with compliance rates, automatic data quality checks, and visualisations. Optionally exports participant-level compliance and payment calculations to Excel.

---

## Setup

**Requirements:** R, RStudio, and the following packages:

```r
install.packages(c("tidyverse", "lubridate", "scales", "readxl", "openxlsx"))
```

**Steps:**

1. Place the `.Rmd` file in a folder of your choice
2. Create a `data/` subfolder and put your Avicenna `.csv` export(s) there
3. Open the `.Rmd` in RStudio and update the study settings at the top of the file
4. Knit with `Ctrl+Shift+K`

> The template assumes standard Avicenna column names: `Participant.ID`, `Session.Scheduled.Time`, `Prompt.Time`, `Record.Time`, `Status`.

---

## Trying it out

Set `use_demo_dataset <- TRUE` in the first code chunk to run the tool on simulated data, without needing your own CSV.

---

## Optional modules

| Toggle | What it does |
|---|---|
| `use_multiple_files` | Merge exports from multiple Avicenna Activities |
| `use_external_ids` | Link Avicenna IDs to your own participant codes |
| `use_excel_export` | Save a timestamped `.xlsx` compliance report |
| `use_remuneration` | Add per-beep or threshold-based payment calculations |

Full instructions for each module are in the `.Rmd` file itself.

---

## Acknowledgements

Inspired by ESM compliance tools developed by **Anne Buelow** for the [100 Days Of My Life](https://osf.io/a9g7c/overview) and [PARADOX](https://osf.io/mwpt7/files/m2qwh) studies. Generative AI was used to help draft and refine the code.

Issues and suggestions welcome — please open a GitHub issue or get in touch by email.
