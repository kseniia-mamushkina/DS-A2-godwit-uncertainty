# AI-use and verification log

## Tool and task

Tool: ChatGPT.
Task: DS-A2 — Inference and Uncertainty Notebook.

ChatGPT assisted with Python codes.

## Accepted recommendations

- Resample complete bird histories in the cluster bootstrap to account
  for repeated migration records from the same bird.
- Preserve the record-weighted mean difference as the estimand.
- Distinguish observed-data inference from prospective power simulations.
- Use bird-clustered standard errors for the observed-data hypothesis test.
- Document the retrospective status of the analysis.
- Describe seven days as an educational planning threshold rather than
  a validated ecological cutoff.

## Rejected advice or approaches

Independent-row inference was rejected as the primary real-data method
because some birds contributed repeated records. It was used only in
the explicitly labelled counterexample.

Prospective power simulations were not treated as a test of the
observed difference or as the power of the original clustered study.

## Execution and numerical verification

The notebook was executed in Google Colab.

The verification code was also AI-assisted. It checked:

- Agreement between the reported effect and direct group-mean subtraction.
- Agreement between a manual Welch formula implemented in code and SciPy.
- Reproducibility of the cluster bootstrap with the same seed.
- Agreement between simulated and theoretical sampling standard errors.

These are numerical implementation checks, not evidence that the
sample is representative or that measurement bias is absent.

## Student-performed independent verification

Using a calculator, I subtracted the reported adult mean crossing date
from the juvenile mean:

225.32142857142858 − 176.96 = 48.361428571428576 days.

Rounded to two decimal places, this equals the notebook's reported
difference of 48.36 days.

This check verifies the mean difference only. It does not independently
verify the bootstrap interval or the cluster-robust p-value.
