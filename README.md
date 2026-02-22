# DL Sprint 4.0 Notebooks

A collection of deep learning training notebooks for speech and audio processing tasks.

## Notebooks

| Notebook | Description |
|----------|-------------|
| `finetuning_tugstugi_full_withlrs40.ipynb` | Fine-tuning speech recognition model with LRS40 dataset |
| `kaggle_train_tugstugi.ipynb` | Kaggle training notebook for Tugstugi model |
| `training-pyannote.ipynb` | Speaker diarization training using PyAnnote |
| `moonshine_training.ipynb` | Moonshine model training |
| `fork-of-training-with-peft.ipynb` | Parameter-Efficient Fine-Tuning (PEFT) training |

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/labib116/DL-Sprint-4.0-Notebooks.git
   ```

2. Install dependencies (varies per notebook, check individual notebooks for requirements)

3. Add your Hugging Face token where required:
   ```python
   login(token="YOUR_HF_TOKEN_HERE")
   ```

## Requirements

- Python 3.8+
- PyTorch
- Hugging Face Transformers
- Additional dependencies as specified in each notebook

## License

MIT
