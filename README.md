# DS-A2: Black-tailed Godwit Migration Timing

This project quantifies uncertainty in the difference between juvenile
and adult Black-tailed Godwit southward migration timing.

## Data

Source: Verhoeven et al. (2021), Dryad.
https://doi.org/10.5061/dryad.02v6wwq4j

License: CC0.

The analysis uses southward crossings of 52°N in 2016–2017:
78 migration records from 71 birds.

## Analysis

- Individual-cluster bootstrap confidence interval.
- Observed-data hypothesis test with bird-clustered standard errors.
- Simulation of a sampling distribution.
- Power analysis varying sample size, noise and effect.
- Dependence counterexample and numerical verification.

The observed juvenile-minus-adult difference was 48.36 days,
with a 95% cluster-bootstrap interval of 42.72–54.08 days.

This is a retrospective continuation of DS-A1. Selection,
measurement and pooled-year limitations restrict interpretation.

## Files

- DS_A2_godwit_uncertainty.ipynb: executable notebook with outputs.
- DS_A2_PDF_report.pdf: report.
- 2.Adult_and_juvenile_timing_forR(1).csv: source data.
- outputs/: figures, numerical results and simulation outputs.
- requirements.txt: recorded Python package versions.
- AI_use_log.md: AI-use and verification record.

## Reproduction

1. Download or clone this repository.
2. Place the source CSV in the same directory as the notebook.
   The filename without "(1)" is also accepted.
3. Use the Python version recorded in outputs/settings.json.
4. Install dependencies with:
   pip install -r requirements.txt
5. Open the notebook in Jupyter and run all cells from top to bottom.

Alternatively, upload the notebook and CSV to Google Colab and run
all cells. The notebook records the active package versions.

The code checks the input SHA-256, fixes random seeds and writes
results to outputs/. Simulation outputs may differ across environments;
the recorded environment should be used for exact reproduction.
