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

## Licence status

Author-owned code: MIT proposed, awaiting rights-holder confirmation.
Author-owned result summaries: CC BY 4.0 proposed, awaiting confirmation.
Until confirmation, no new blanket permission is granted for author-owned work.
Third-party notices and permissions remain effective under their original terms;
the probabilistic-baseline attribution is retained in the code archive.

## Contact

Corresponding author: Yingqiang Cai, cai202@jmu.edu.cn.
ORCID: https://orcid.org/0000-0002-8409-996X
