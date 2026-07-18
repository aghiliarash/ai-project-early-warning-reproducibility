# AI Project Early-Warning Reproducibility Package

Reproducibility materials for **“Archival Early-Warning Signals of Implementation Distress in AI Projects: A Mixed-Methods Study of Resistance, Governance Enactment, and Project Outcomes.”**

## Scope

This repository provides an auditable computational workflow, documentation, disclosure-controlled outputs, and a **synthetic demonstration dataset**. It does **not** provide open-data replication of the original empirical estimates. Original archival project records and interview materials are restricted because they contain confidential organizational and employee-related information.

The supplied synthetic data are artificial. They are not calibrated to reproduce the study’s observed correlations, coefficients, threshold location, performance estimates, or published tables. They exist only to let users execute and inspect the workflow.

## What the workflow does

- validates the data dictionary and temporal fields;
- assesses missingness and uses training-fold-only imputation;
- estimates organization-clustered associational models;
- evaluates a binary adverse-project-outcome model using repeated, nested, organization-blocked cross-validation;
- reports discrimination, calibration, classification metrics, and uncertainty summaries;
- computes held-out permutation importance;
- produces data-support, ALE-style, ICE-style, and bootstrap candidate-threshold outputs;
- exports tables and figures to `outputs/`.

## Important interpretation limits

The model is predictive and associational. Feature importance is not causal evidence. A BARS value near 5 is evaluated only as an exploratory candidate alert point; this workflow does not validate a universal threshold. Synthetic-data outputs must not be cited as empirical replication of the study.

## Quick start

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python code/01_generate_synthetic_demo_data.py
python code/02_run_demo_pipeline.py
```

## Restricted-data access

A request for access to de-identified original data must be evaluated under organizational permission, ethical requirements, and applicable data-protection obligations. See `documentation/controlled_access_protocol.md`.

## Citation


