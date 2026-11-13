# Kenya Electoral Participation Analytics

A reproducible Python analysis of county-level presidential
electoral participation in Kenya across the 2013, August 2017,
October 2017 and 2022 elections.

## Project Overview

The study investigates changes in registered voters, valid
presidential votes and participation rates across Kenya's
47 counties.

### Headline Findings

- **47 of 47 counties** recorded declining valid-vote
  participation between 2013 and 2022.
- Registered voters increased by
  **53.69%**.
- Valid presidential votes increased by
  **16.27%**.
- Weighted valid-vote participation fell by
  **20.68
  percentage points**.

## Methods

The project uses Python and pandas for data preparation,
reconciliation and analysis, with Matplotlib for visualisation.

Valid-vote participation is defined as:

`valid presidential votes / registered voters * 100`

It is not equivalent to ballots-cast turnout.

## Project Structure

```text
kenya-electoral-participation-analytics/
├── data/
│   ├── interim/
│   └── processed/
├── documentation/
├── notebooks/
│   ├── 01_elog_data_extraction_validation.ipynb
│   ├── 02_official_source_reconciliation.ipynb
│   ├── 03_election_data_preparation.ipynb
│   ├── 04_exploratory_electoral_participation_analysis.ipynb
│   ├── 05_electoral_participation_visualisation_reporting.ipynb
│   └── 06_final_project_synthesis_source_verification.ipynb
├── reports/
│   ├── figures/
│   ├── kenya_electoral_participation_portfolio_report.md
│   └── notebook05_findings_report.md
├── PROJECT_BRIEF.pdf
├── README.md
├── requirements.txt
└── .gitignore
```

**Source availability:** The original `data/raw/` directory
is retained locally and excluded from GitHub. The repository
includes intermediate datasets, processed data, reconciliation
outputs and validation documentation.


## Analysis Workflow

1. Extract and validate ELOG county election results.
2. Reconcile historical figures against IEBC materials.
3. Prepare the integrated analytical dataset.
4. Analyse participation trends and county differences.
5. Produce and verify five analytical visualisations.
6. Reconcile 2022 figures and perform sensitivity checks.

## Analytical Coverage

The direct 2013–2022 endpoint comparison covers all
47 counties.

Comparisons requiring August 2017 figures use 45 counties
because Kisumu and Turkana have unresolved August 2017
source discrepancies.

October 2017 is treated as a distinct fresh presidential
election, not an ordinary general election.

## Data Quality and Source Assurance

The project retains documented discrepancies instead of
silently correcting source figures.

For 2022, ELOG county registration and reported valid-vote
figures match the Takwimu transcription in all 47 counties.
The original signed Form 34C has not been independently
authenticated.

Detailed reconciliation and validation records are
available in `documentation/`.

## Main Report

[Read the portfolio report](
reports/kenya_electoral_participation_portfolio_report.md
)

## Visualisations

Five verified figures are available in `reports/figures/`.

## Reproducing the Analysis

Run the six notebooks in numerical order from the
`notebooks/` directory.

The notebooks expect the project folder structure shown
above and the original source files under `data/Raw/`.

The analysis requires a Python environment with the
libraries imported by the notebooks, including pandas,
NumPy and Matplotlib.

## Interpretation

This is a descriptive electoral participation study.
It does not identify the causes of changes in voting
behaviour or establish causal relationships.

## Environment Setup

The project was developed using Python with the package
versions recorded in `requirements.txt`.

To create a local environment:

```bash
python -m venv .venv
```

Activate the environment on Windows:

```powershell
.venv\Scripts\Activate.ps1
```

Install the required packages:

```bash
python -m pip install -r requirements.txt
```

Start JupyterLab:

```bash
jupyter lab
```

Run the notebooks in numerical order, beginning with
Notebook 01.

**Note:** The notebooks use local project paths and expect
the original source documents to be available in the
appropriate `data/raw/` directories. Some source PDFs
are not included in the public repository.

## Source Documents and Redistribution

The project draws on ELOG electoral reports, IEBC
publications and a 2022 secondary transcription attributed
to IEBC Form 34C.

The entire `data/raw/` directory is excluded from the
public repository pending review of source redistribution
rights. This includes original reference PDFs and the
2022 secondary-source CSV transcription.

Intermediate datasets, the final processed analytical
dataset, reconciliation tables and validation outputs
remain available in the repository.

Notebooks 01–03 require the original source files for
complete end-to-end reproduction. Notebooks 04–06 can
be examined alongside the published analytical outputs.

The analysis retains documented reconciliation differences,
including unresolved August 2017 figures for Kisumu and
Turkana.

The 2022 ELOG and Takwimu county registration and reported
valid-vote totals match across all 47 counties. This
constitutes secondary-source corroboration, not independent
authentication of the original signed Form 34C.

Users seeking to reproduce the extraction stages should
obtain the original source documents from their publishers
and review the source references in the project notebooks.
