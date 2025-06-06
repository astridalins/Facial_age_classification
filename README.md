FACIAL AGE CLASSIFICATION
This project focuses on facial age prediction using convolutional neural networks (CNNs). Two classification tasks are explored:
    100 exact ages (from 0 to 99)
    11 age groups (e.g., 0–9, 10–19, ..., 90+)

Different CNN architectures were tested, along with various training phases, fine-tuning strategies, and data augmentation techniques.


Project Structure:
    FACIAL AGE CLASSIFICATION/
    │
    ├── REPORT.docx
    │   → Project report describing methodology, results, and conclusions.
    │
    ├── CODE/
    │   ├── Original Architecture _ Original +1 FC _ Original + 2FC.ipynb
    │   │   → Experiments with different fully connected layer configurations.
    │   │
    │   ├── 11_outputs.ipynb
    │   │   → Training and evaluation for 11-age-group classification.
    │   │
    │   └── RESULTS/
    │       ├── initial_weights.weights.h5
    │       │   → Pretrained weights used for transfer learning.
    │       │
    │       ├── 11_outputs/
    │       │   ├── Second Phase/
    │       │   └── With data augmentation (Second Phase)/
    │       │       → Training history, final model weights and plots.
    │       │
    │       └── 100_outputs/
    │           ├── Original CNN/
    │           │   ├── Finetune_last_convolutional_block (not enough)/
    │           │   └── 1st conv block + part of 2nd block frozen/
    │           │       → First Phase / Second Phase results.
    │           │
    │           ├── Original CNN + 1FC/
    │           │   → First and Second Phase with and without augmentation.
    │           │
    │           └── Original CNN + 2FC/
    │               → Results for different phases and configurations.


Notebook Notes – Evaluation & Usage Instructions

    This project includes two main Jupyter notebooks:
        -Original Architecture _ Original +1 FC _ Original + 2FC.ipynb
        -11_outputs.ipynb

    Both are structured for manual and modular analysis, not full training pipelines. The results (weights, plots, metrics) are already available in the RESULTS/ folder. These notebooks are mainly intended for:

        Loading and evaluating trained models
        Visualizing class distributions
        Computing tolerance-based accuracy and MAE
        Comparing architectural variants

    Section 5 – Model & Weights Must Match
    ⚠️ IMPORTANT: Before running any block in Section 5, ensure the selected model architecture matches the weights you're loading.

    For instance:
    If using Original CNN + 1FC, you must load weights from
    RESULTS/100_outputs/Original CNN + 1FC/...

    Mismatching architectures and weights will cause incorrect behavior or runtime errors.
    These notebooks support flexible experimentation, but it is the user's responsibility to maintain consistency between architecture and weights.

    📘 11_outputs.ipynb – Additional Notes
        Section 6 – Example of a Training Block
        ⚠️ Note: This block is only an illustration of the training logic.
        It is not meant to be run directly, as the training process was already completed and the results are provided under RESULTS/.