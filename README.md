# Long-Form Bengali ASR and Speaker Diarization Experiments

Training notebooks from Team Villagers' submission to BUET CSE Fest DL Sprint 4.0. The work investigates model selection, fine-tuning, acoustic augmentation, and post-processing for long-form Bengali automatic speech recognition (ASR) and speaker diarization.

Team Villagers placed **2nd Runner-Up** and received the **Best Dataset Award**. The experiments are connected to the paper and Lipi-Ghor-882 dataset described below. This repository contains working and exploratory notebooks; it is not yet a one-command reproduction package for every result in the paper.

## Problem

Long-form Bengali audio combines transcription, speaker-boundary detection, noise, reverberation, overlapping speech, and strict runtime constraints. The project evaluates practical ASR and diarization pipelines for this low-resource setting.

## Experimental approach

The notebooks cover:

- evaluation and fine-tuning of Bengali ASR checkpoints;
- synthetic acoustic degradation, including noise and reverberation;
- parameter-efficient fine-tuning experiments;
- Moonshine experiments;
- Pyannote-based speaker-diarization training.

The related paper reports that carefully aligned data with targeted acoustic augmentation was more effective for ASR than raw data scaling, while heuristic post-processing was central to the final diarization pipeline. Refer to the paper for the complete experimental claims and limitations.

## Notebooks

| Notebook | Scope |
|---|---|
| `finetuning_tugstugi_full_withlrs40.ipynb` | Bengali ASR fine-tuning with the LRS40-related experimental data |
| `kaggle_train_tugstugi.ipynb` | Kaggle training workflow for a Tugstugi Bengali ASR checkpoint |
| `training-pyannote.ipynb` | Pyannote speaker-diarization training experiments |
| `moonshine_training.ipynb` | Moonshine ASR experiments |
| `fork-of-training-with-peft.ipynb` | Parameter-efficient fine-tuning experiments |

## Data

The paper introduces **Lipi-Ghor-882**, an 882-hour multi-speaker Bengali dataset. Data is not bundled in this repository. Some notebooks expect datasets mounted under Kaggle-specific paths; adjust the path variables for your environment and consult the paper and dataset release for access conditions.

## Reproduction status

These notebooks preserve the team's experiment workflows, but they currently retain platform-specific paths and execution outputs. Reproduction may require:

1. A CUDA-capable environment and sufficient GPU memory.
2. The corresponding competition or Lipi-Ghor-882 data.
3. Access to the pretrained checkpoints referenced inside each notebook.
4. Updating dataset/output path variables for the local platform.
5. Installing the dependencies declared in the first setup cells.

Tokens must be supplied through platform secrets or environment variables. Do not place credentials directly in notebooks.

## Related publication

Sanjid Hasan, Risalat Labib, A H M Fuad, and Bayazid Hasan. **“Make It Hard to Hear, Easy to Learn: Long-Form Bengali ASR and Speaker Diarization via Extreme Augmentation and Perfect Alignment.”** arXiv:2602.23070, 2026.

- [Abstract and paper](https://arxiv.org/abs/2602.23070)
- [DOI](https://doi.org/10.48550/arXiv.2602.23070)

## Team and attribution

This was a team project by **Team Villagers**. The repository and publication should be cited as team work; no claim of sole individual contribution is made here. Pretrained models, libraries, and external datasets remain the work of their respective authors and maintainers.

## Limitations

- The notebooks are experiment artifacts rather than a unified training package.
- Environment versions are not yet locked in a single requirements file.
- Platform-specific paths still require manual configuration.
- Not every paper result can currently be regenerated from a single notebook.

## License

Code in this repository is released under the MIT License where compatible with the licenses of external models, datasets, and competition materials. Those external assets retain their original terms.
