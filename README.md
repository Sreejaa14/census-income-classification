# Census Income Classification (PyTorch)

A binary classifier for predicting whether a person earns more than $50,000 annually, using the Census Income dataset.

## Repository structure

```text
census_income_workshop/
├── income.csv                         # Add the dataset here; do not commit private/sensitive data
├── notebooks/
│   └── census_income_workshop.ipynb
├── requirements.txt
└── README.md
```

## Dataset

Download `income.csv` from the assignment's [Google Drive dataset](https://drive.google.com/file/d/1ay5vOv2YiOwjKIWnXFT6sptW0gqew0oa/view?usp=sharing) and place it in the repository root. The notebook expects 30,000 rows and uses 25,000 for training and 5,000 for testing.

## Setup

Python 3.10 or newer is recommended.

```bash
python -m venv .venv
# Windows: .venv\\Scripts\\activate
# macOS/Linux:
source .venv/bin/activate
pip install -r requirements.txt
```

## Run

From the repository root:

```bash
jupyter notebook
```

Open `notebooks/census_income_workshop.ipynb` and run all cells. If the target column is not detected correctly, set `TARGET_COLUMN` in the notebook to the actual label column name. Review the printed label mapping before training.

## Model

- Categorical predictors: learned embeddings
- Continuous predictors: batch normalization
- Hidden layer: 50 neurons with ReLU
- Dropout: 0.4
- Output: two logits, trained with CrossEntropyLoss
- Optimizer: Adam, learning rate 0.001
- Training: 300 epochs
- Evaluation: test loss and accuracy

## Submission

Commit the notebook, `requirements.txt`, and this README to GitHub. Run all notebook cells first so the notebook contains the actual results from your copy of `income.csv`. Then submit the GitHub repository URL in the Moodle workshop submission box.

Do not commit credentials or any data you are not permitted to share.
