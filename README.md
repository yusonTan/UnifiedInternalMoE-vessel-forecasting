# UnifiedInternalMoE vessel trajectory forecasting

Reproducibility materials for heterogeneous mixture-of-experts long-horizon
vessel trajectory forecasting. Each regional task is trained independently:
the shared architecture is not a single cross-region checkpoint.

## Reproduce reported numerical tables

Download `S1_Code.zip` and `S1_Data.zip` and extract both into one empty directory.
Using Python 3.11, from that directory run:

```sh
python reproduce.py verify --manifest CORE_MANIFEST.json
python reproduce.py tables --out regenerated
```

Table reconstruction uses the Python standard library. Model smoke tests,
inference and optional training require the scientific environment described in
the extracted README and requirements. Historical campaign launchers preserve
their original paths as provenance; use `reproduce.py` for portable entry points.

## Contents and cohorts

The code archive contains source snapshots, configurations, plotting code,
portable entry points and a combined checksum manifest. The data archive contains
the numerical CSV results for the completed comparison/control experiments.
Four-region main comparisons, routing, capacity and source-domain transfer use
ten seeds. Internal ablations, the probabilistic comparator and independent
Finnish validation use five seeds. Historical three-seed diagnostics are separate.
The archive preserves unfavourable as well as favourable controls.

These two archives do not include raw AIS, per-window trajectory arrays, all
paired-error arrays, trained checkpoints or replay inputs. They reproduce the
reported mean/SD tables, not every full-data prediction from scratch. Additional
prediction-level assets require a separately documented deposit; do not infer
that the small CSV archive alone supports re-running all uncertainty analyses.

## Upstream data and rights

EnvShip v2 Track B:
https://huggingface.co/datasets/mark000071/envship_v2_datasets

Independent Finnish AIS:
https://doi.org/10.5281/zenodo.8112336

See `DATA_RIGHTS.md` and the archived upstream notices inside S1_Code.zip.
The Finnish dataset is CC BY 4.0. EnvShip has component-specific terms and must
not be described as uniformly CC BY. This repository does not mirror raw AIS.
The upstream dataset DOI is not the DOI of this project's code or results.

## Licences

Author-owned code is released under the MIT licence; see `LICENSE`.
Author-owned numerical result summaries are released under CC BY 4.0;
see `LICENSE-DATA.md`. These scopes apply to the contents of the archives too.
Third-party notices and permissions remain effective under their original terms;
the probabilistic-baseline attribution is retained in the code archive.

## Citation

If you use this method, code or result tables in a research publication, please
cite this repository and the associated paper when its public bibliographic
record is available. Use `CITATION.cff` (GitHub's **Cite this repository**) or
`CITATION.bib`. Identify the commit used for reproducibility. We have not assigned
a journal, publication status or DOI to an unpublished manuscript. This academic
citation request does not add a condition to the MIT licence.

## Contact

Corresponding author: Yingqiang Cai, cai202@jmu.edu.cn.
ORCID: https://orcid.org/0000-0002-8409-996X
