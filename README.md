# How Robust Is the Evidence that Algorithmic Control Displaces Responsibility?

An exploratory secondary analysis of two experiments examining algorithmic autonomy, unethical choices, and responsibility attribution.

**Project 16 — Team Spiderman**

- Nikhilesh Krishnamurthy Iyer
- Bhanu Prasad Mudraboina

## Overview

This project examines whether findings about algorithmic autonomy restriction remain stable across alternative statistical models, responsibility measures, and participant-screening rules.

We analyse the author-released data from both experiments in Jolly, Dunlop, Parker, and Kanse’s paper, *It’s Not My Responsibility: Working with Autonomy-Restricting Algorithms Facilitates Unethical Behavior and Displacement of Responsibility*.

This reanalysis is exploratory. The original experiments’ registrations do not constitute a preregistration of our secondary analyses.

## Repository contents

| Location | Contents |
| --- | --- |
| `notebooks/project16-team-spiderman-final-kaggle.ipynb` | Final executed notebook covering both studies |
| `Results/` | Verified Kaggle outputs, including 17 tables, 11 PDF figures, and supporting files |
| `Results/requirements.txt` | Pinned analysis dependencies |
| `Results/software_versions.json` | Software versions recorded during execution |
| `Results/artifact_index.json` | Output descriptions and filenames |
| `Results/SHA256SUMS.txt` | Checksums for the other 39 files in the results bundle |
| `Results/source_provenance.json` | Dataset sources and expected checksums |
| `data/raw/` | Three original author data files |
| `proposal/Project16_Proposal.docx` | Original project proposal |
| `documentation/` | Supporting project information |
| `CITATION.cff` | Repository citation metadata |
| `LICENSE` | MIT licence for the team’s original code |

The proposal records the original plan. The final notebook and results describe the analyses actually completed.

## Research questions

1. Which autonomy-assignment effects remain stable across alternative statistical models?
2. How does the definition of external responsibility affect the conclusions?
3. Are effects consistent across dilemmas and studies?
4. How do measurement and mediation assumptions constrain interpretation?
5. How sensitive are estimates to participant-screening and exclusion assumptions?

## Data

| File | Purpose |
| --- | --- |
| `Experiment 1 for OSF.sav` | Study 1, with 276 released participants |
| `Experiment 2 for OSF.sav` | Study 2, with 256 released participants |
| `Exp2Data.csv` | Additional Study 2 responsibility analyses and benchmark checks |

The notebook verifies each file against its expected SHA-256 checksum and checks agreement between the Study 2 CSV and SAV records.

The released datasets contain retained participants. Records for the 13 excluded Study 1 participants and 12 excluded Study 2 participants are unavailable. Their possible influence is assessed using bounds.

Original data and materials are available through the [authors’ OSF project](https://osf.io/phg82/?view_only=4f847ddbc31d490b90917809c4e07c38). Consult that source for data access and reuse terms.

## Run on Kaggle

1. Import `notebooks/project16-team-spiderman-final-kaggle.ipynb`.
2. Select Python, use no accelerator, and enable Internet.
3. Attach the three original data files as a Kaggle input, keeping their filenames unchanged. The notebook also attempts verified OSF downloads when files are unavailable locally.
4. Choose **Run All**.
5. If setup requests a kernel restart after installing packages, restart the session and choose **Run All** again.
6. Download `project16_results.zip` using the link displayed by the final cell.

The notebook searches Kaggle input folders automatically. For offline use, attach all three data files and install the pinned packages before disabling Internet.

The final archive contains 40 files, including 28 indexed outputs and 12 supporting files. Source datasets are excluded from that generated results archive.

## Run locally

Use Python 3.12 or 3.13 with Jupyter/IPython installed.

Install the analysis dependencies from `Results/requirements.txt`. Before running the notebook, set the environment variable `PROJECT16_INPUT_DIR` to the absolute path of the repository’s `data/raw` directory.

Alternatively, place the three original files in a `project16_source` folder in the notebook’s working directory.

The setup cell installs missing or mismatched analysis packages by default. Use a fresh kernel.

## Verified execution

The submitted Kaggle notebook contains 15 executed code cells.

| Check | Study 1 | Study 2 |
| --- | ---: | ---: |
| Released participants | 276 | 256 |
| Completed behavioral specifications | 36/36 | 36/36 |
| Failed or nonconverged specifications | 0 | 0 |
| Restricted-minus-affording probability differences across specifications | 0.273–0.307 | 0.263–0.320 |

The analysis uses seed `16026` and 2,000 participant bootstrap replicates where specified.

All 39 checksums recorded in `Results/SHA256SUMS.txt` were verified against the uploaded results.

## Findings and interpretation

Restricted autonomy was associated with a higher probability of unethical choices across all 72 behavioral specifications. These specifications share data and provide dependent evidence.

In Study 2, additional unethical choices were associated with lower subsequent self-responsibility and higher maximum external responsibility after adjustment for assignment and earlier ratings.

Some alternative external-responsibility measures had confidence intervals crossing zero. Direct paired comparisons between the maximum and alternative external measures also included zero. These results should be interpreted together.

Choice-count slopes, mediation estimates, and responsibility-rating relationships are exploratory associations. Random assignment to autonomy conditions does not establish that observed unethical choices causally changed subsequent responsibility ratings.

## Reproduction limitations

The H1 and H2 component benchmarks fall within the notebook’s stated tolerance.

Two Study 2 Figure 5 coefficient comparisons fall outside the printed-rounding tolerance.

| Component | Published benchmark | Recomputed |
| --- | ---: | ---: |
| Autonomy coefficient in the unethical-choice equation | −1.15 | −1.16635 |
| Earlier self-responsibility coefficient in the later self-responsibility equation | 0.67 | 0.67542 |

The notebook uses separate component regressions. Exact reproduction of the original joint Mplus model and its inference requires the original Mplus estimation procedure.

Additional limitations include post-assignment screening, unavailable excluded records, pointwise exploratory intervals, and the simulated hotel-service setting. Screening bounds do not include sampling uncertainty.

## Citation and attribution

Use `CITATION.cff` to cite this repository.

Anchor paper:

Jolly, A. A., Dunlop, P. D., Parker, S. K., and Kanse, L. (2026). *It’s Not My Responsibility: Working with Autonomy-Restricting Algorithms Facilitates Unethical Behavior and Displacement of Responsibility*. Journal of Business Ethics, 203, 405–424. First published online in 2025.

https://doi.org/10.1007/s10551-025-06034-5

The MIT licence covers the team’s original code. Third-party data and materials retain their original attribution and applicable reuse terms.

Target journal: Journal of Business Ethics.
