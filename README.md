# Explainable Machine Learning for Gait-Based MCI Identification

This repository is a privacy-preserving research portfolio for an ongoing project on identifying mild cognitive impairment (MCI) from ordinary dual-task walking videos. It presents the study design, analytical workflow, and selected aggregate results without releasing participant-level data, identifiable gait records, or the unpublished manuscript.

> **Status:** Manuscript in preparation. This repository is intended for research-portfolio review and is not a clinical diagnostic tool.

## Research question

Can micro-level, whole-body gait markers extracted from standard video support non-invasive MCI screening while remaining interpretable and temporally reliable?

## Project highlights

- Analyzed a cohort of 369 older adults: 188 participants with MCI and 181 cognitively normal controls.
- Extracted 2,640 time- and frequency-domain gait features from OpenPose skeletal keypoints.
- Applied a two-stage ANOVA and recursive feature elimination workflow to retain 50 discriminative features.
- Compared seven classification algorithms, including Logistic Regression, SVM, Random Forest, LightGBM, XGBoost, MLP, and KNN.
- The selected Logistic Regression model achieved 0.842 recall and 0.711 AUC on an independent test set.
- Used SHAP to identify interpretable behavioral indicators involving lower-limb asymmetry, upper-limb rhythmic coordination, and head stability.
- Obtained split-half reliability of 0.930 (p < 0.001) using odd- and even-frame subsequences.

## Siqi Ma's contributions

Siqi Ma contributed to skeletal-keypoint data preparation with OpenPose, ANOVA-RFE feature selection, comparison of seven machine-learning algorithms, model evaluation, SHAP-based interpretation, reliability analysis, and manuscript preparation.

## Analytical workflow

1. Standardize dual-task gait videos and extract stable frame sequences.
2. Derive OpenPose whole-body skeletal keypoints.
3. Construct coordinate, velocity, inter-joint distance, and joint-angle time series.
4. Extract time- and frequency-domain descriptors.
5. Perform ANOVA screening followed by recursive feature elimination.
6. Train and compare seven classifiers using repeated stratified cross-validation.
7. Evaluate the selected model on an independent test set.
8. Interpret feature contributions with SHAP and assess temporal split-half reliability.

## Repository contents

```text
figures/
  anatomical-feature-map.png
  shap-feature-importance.png
README.md
DATA_PRIVACY.md
```

## Data availability and privacy

The underlying data contain participant names and high-dimensional behavioral measurements collected in a health-research context. They are therefore excluded from this repository. No raw videos, skeletal trajectories, participant identifiers, clinical labels, or row-level feature data are provided.

Researchers interested in the data should contact the study's principal investigator and follow the applicable institutional ethics and data-access procedures.

## Responsible-use notice

The findings are preliminary and have not yet completed peer review. They should not be used for clinical diagnosis, treatment decisions, or claims about individual cognitive status.

## License

No open-source license is currently granted. All rights are reserved while manuscript, data-ownership, and collaboration permissions are being confirmed.
