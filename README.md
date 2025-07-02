# HCI18_SEGMENTATION

## Project Structure

```
├── data/                   # HCI18 Dataset
│   ├── training_set/
│   ├── test_set/
│   ├── test_set_pixel_size.csv
│   ├── training_set_pixel_size_and_HC.csv
│   ├── training_mask/
│   ├── test_set_result.csv
├── docs/                   # Requirement libs
│   ├── requirements.txt
├── logs/                   # Training logs
├── notebooks/              # Jupyter notebooks
│   ├── config.yaml
│   ├── data_exploration.ipynb
│   ├── model_build.ipynb
├── src/                    # Python scripts
│   ├── utils/
│   │   ├── dice_loss.py
│   │   ├── learning_curve.py
│   │   ├── masking_annotation.py
│   │   ├── predict.py
│   ├── config.yaml
│   ├── data_loader.py
│   ├── unet_model.py
│   ├── train.py
├── report/                    # Project Report
│   ├── figures/
│   ├── report_2.pdf
│   ├── report_2.tex
└── .gitattributes
```

## Setup

**Install dependencies**
   ```bash
   git clone https://github.com/DungeonLeiz/HCI18_Segmentation.git
   cd HCI18_Segmentation/docs
   pip/pip3 install -r requirements.txt
   ```

## Usage

### Unet Training
Train a Unet model from scratch:
```bash
cd src/
python/python3 train.py
```

### Unet Testing & Metrics
Run detailed evaluation, confusion matrix, and save predictions:
```bash
cd src/utils/
python/python3 predict.py
```