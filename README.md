# ZooBot Fine-Tuning on NGVS Morphology Labels (Curated Example)

This repository contains  curated examplse of fine-tuning a pretrained ZooBot CNN on galaxy cutouts from the Next Generation Virgo Cluster Survey (NGVS), generating predictions, and inspecting model failure cases with goal of offering interpretaibltiy and high resolution learned morphologies for use with current and upcoming large galaxy surveys.

## What is including
- Building a ZooBot-compatible `catalog` (`id_str`, `file_loc`, label columns)
- Fine-tuning a pretrained CNN under domain shift and heterogeneous image quality
- Saving predictions for reproducible downstream analysis
- Qualitative error inspection (top/bottom confidence cases; incorrect vs correct)

## Contents
- `notebooks/ZooBotNGVS_Curated_Example.ipynb` — main workflow (end-to-end)
- `outputs/figures/` — curated qualitative inspection figures
- `outputs/tables/` — prediction CSVs and optional summary metrics

## Running the notebook
1. Create an environment with PyTorch + ZooBot dependencies.
2. In the notebook, set:
   - `DATA_DIR` (image directory)
   - `CATALOG_CSV` (metadata + labels)
   - `CHECKPOINT_LOC` (pretrained ZooBot checkpoint)
3. Run cells top-to-bottom. Predictions will be written to:
   - `outputs/run_001/finetuned_predictions.csv`
   - `outputs/run_001/figures/top_confidence.png`
   - `outputs/run_001/figures/bottom_confidence.png`

## Notes
- Image data are not included in this repository.
- This is research code intended to highlight transparent evaluation and failure analysis rather than production deployment.
