# Data sources and release boundaries

Checked 17 October 2026. These notes record the upstream terms; they do not grant
new third-party permissions or replace the original notices.

## EnvShip v2 Track B

Public source: https://huggingface.co/datasets/mark000071/envship_v2_datasets

Authoritative mapping:
https://huggingface.co/datasets/mark000071/envship_v2_datasets/blob/main/LICENSE-DATA.md

Required credits:
https://huggingface.co/datasets/mark000071/envship_v2_datasets/blob/main/NOTICE.md

The release has composite, not blanket CC BY, licensing. Its AIS components
follow the source terms: DMA Danish public-sector information; NOAA U.S.
government public-domain material; Piraeus CC BY 4.0; Norway NLOD 2.0. Preserve
source attribution and the original limitations. OSM-derived context/columns
have separate ODbL obligations; reanalysis columns have separate upstream terms.
Our predictor uses trajectory/kinematic inputs rather than those context tensors.

For the first public code release, link to the upstream dataset instead of
mirroring raw tables, local replay inputs or target trajectory arrays. This
avoids relicensing mixed upstream tables under the code licence. It does not
imply that the upstream dataset is closed or that all redistribution is forbidden.
The current upstream revision is recorded in release_audit/AUDIT.json. Its
identity with the original experimental input files has not yet been verified.
Do not silently use a new revision as an exact substitute for those inputs.

## Independent Finnish AIS

Bhattacharya, Debayan; Ul Haq, Ikram; Pichardo Vicencio, Carlos; Lafond, Sebastien.
A Large-Scale AIS Datset from Finnish Water. Zenodo, v1.
https://doi.org/10.5281/zenodo.8112336

The Zenodo API specifies CC BY 4.0:
https://creativecommons.org/licenses/by/4.0/

Redistribution/adaptation is permitted subject to attribution, licence notice
and disclosure of changes; other applicable rights remain unaffected. This
study uses 19–25 April 2021, filters moving-vessel records, excludes source-domain
MMSIs, segments and interpolates tracks, transforms coordinates, and creates
MMSI-disjoint windows. It is not the entire original release. Retain these
modification notes with any redistributed derived subset.

## Code and results are separate

MIT is proposed for author-owned code; author-owned numerical summaries are
proposed for CC BY 4.0. Neither proposal is active until the rights holder
confirms. Neither licence overrides the third-party terms above. Retain the
probabilistic-baseline attribution and MIT copyright notice bundled in
release_audit/PROBABILISTIC_MDN_NOTICE.md. Other scientific dependencies retain
their own licences and are installed, not redistributed as this project's code.

## Publication state

The lightweight code and numerical-table archives are publicly available at
https://github.com/yusonTan/UnifiedInternalMoE-vessel-forecasting.
Rights-holder licence confirmation is still pending; no project DOI exists.
The upstream data DOI is not the DOI of this project's code or experiment results.
