# Robustness of algorithmic control and responsibility

This reproducibility archive contains the completed exploratory secondary analysis of two experiments on autonomy restriction, unethical choices, and responsibility attribution.

## Files

- `Project16_Final_Analysis.ipynb` contains the team's final executed Kaggle run with 16 code cells, 16 displayed tables, and 11 figures.
- `project16_revised_results.zip` contains the aggregate PDF, PNG, and CSV outputs and provenance records. These exports were generated in an independently verified local run of the same code. The Kaggle tables agree with those exports to displayed precision.
- `requirements.txt` lists the analysis dependencies for local use.
- `SHA256SUMS.txt` records the checksums of the archive contents.
-  [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24460669.svg)](https://doi.org/10.5281/zenodo.24460669)

## Reproduce the analysis

Import the notebook into Kaggle, use Python on CPU, enable Internet, and select Run All. The data loader verifies each of the three author files against its SHA-256 checksum. To work from attached files, follow the instructions under Acquire verified author files and set `ALLOW_OSF_DOWNLOADS = False`. Install the required packages before running offline.

The final cell writes `project16_revised_results.zip`. The archive contains 25 research outputs and two audit or benchmark tables. All 72 behavioral specifications converged in the executed run. The seed is 16026 and the participant bootstrap uses 2000 replicates. Package versions appear in the executed notebook and in the results archive.

## Interpretation and provenance

Study 2 H3 estimates are unstandardized OLS component regressions compared with Figure 5 of the anchor paper. The paired comparisons are exploratory. Randomized assignment contrasts and associations conditional on earlier responsibility ratings address different questions. The release omits the excluded participant records, so the analysis reports bounds for their possible influence.

The author files are available from the project linked in the paper. This archive contains aggregate outputs. Consult the source project for data access and reuse terms.

Target journal: Journal of Business Ethics (Springer Nature).

Anchor paper: Jolly, Dunlop, Parker, and Kanse (2026). https://doi.org/10.1007/s10551-025-06034-5

Data source: https://osf.io/phg82/?view_only=4f847ddbc31d490b90917809c4e07c38
