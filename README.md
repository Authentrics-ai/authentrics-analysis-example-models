# Authentrics analysis example models (data-only)

This repository is **data-only**: it contains zipped model artifacts and related files that you can download to run the Authentrics analysis examples.

The actual runnable code and instructions live in the examples repo: [Authentrics-ai/authentrics-analysis-examples](https://github.com/Authentrics-ai/authentrics-analysis-examples)

## Downloads (zip files in this repo)

- **CNN dataset (used for both ONNX + TORCH MilitaryAircraft models)**: [Military Aircraft Detection Dataset (Kaggle)](https://www.kaggle.com/datasets/a2015003713/militaryaircraftdetectiondataset)
  - `./ONNX_MilitaryAircraft.zip`
  - `./TORCH_MilitaryAircraft.zip`

- **LLM dataset (used for the HF MedicalChatbot model)**: [FirstAidInstructionsDataset, iCliniq subset (Hugging Face)](https://huggingface.co/datasets/lextale/FirstAidInstructionsDataset/viewer/default/icliniqDataset)
  - `./HF_MedicalChatbot.zip`

## What’s inside each archive

Each `.zip` includes:

- **Model artifacts** (used by the examples repo)
- **Sample inputs** (small, representative data)
- **Expected outputs** for those samples

### HF `MedicalChatbot` archive format

- **Sample data**: a `.jsonl` file (one JSON record per line)
- **Expected output**: a `.txt` file with **one response per line**, aligned to the `.jsonl` line order (line _N_ corresponds to `.jsonl` line _N_)

### ONNX / TORCH `MilitaryAircraft` archive format

- **Sample data**: images of military aircraft
- **Expected output**: a **one-hot encoded matrix** of **20 classes**
  - **one row per sample**
  - rows are ordered by **alphabetical filename order** of the sample images

## How to download

- Download directly from GitHub’s UI (open any `.zip` above and use **Download**), or clone the repo:

```bash
git clone https://github.com/Authentrics-ai/authentrics-analysis-example-models.git
cd authentrics-analysis-example-models
ls -lh *.zip
```

> Note: The archives are stored using Git LFS as they are over 200MB each. The TORCH archive in particular is over 800MB as it includes the optimizer state.
