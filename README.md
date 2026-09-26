# MAGIC Gamma Telescope — Machine Learning Classification

This project applies several machine learning classification algorithms to the **MAGIC Gamma Telescope** dataset. The goal is to classify telescope observations as either **gamma-ray signal** or **hadron background**.

The project contains separate Jupyter notebooks implementing and evaluating multiple machine learning approaches.

## Dataset

The **MAGIC Gamma Telescope** dataset was created using Monte Carlo simulations to model the registration of high-energy gamma particles in a ground-based atmospheric Cherenkov telescope.

The dataset contains measurements describing the shape and characteristics of particle shower images recorded by the telescope. These measurements can be used to distinguish gamma-ray events from hadronic background events.

### Dataset Information

| Property       | Description                |
| -------------- | -------------------------- |
| Dataset        | MAGIC Gamma Telescope      |
| Instances      | 19,020                     |
| Features       | 10                         |
| Feature Type   | Real-valued                |
| Dataset Type   | Multivariate               |
| Task           | Classification             |
| Missing Values | None                       |
| Target Classes | Gamma (`g`) / Hadron (`h`) |

The dataset was created by R. Bock and is available through the UCI Machine Learning Repository.

**Dataset citation:**

> Bock, R. (2004). *MAGIC Gamma Telescope* [Dataset]. UCI Machine Learning Repository. DOI: 10.24432/C52C8B.

**Official dataset page:** UCI Machine Learning Repository — MAGIC Gamma Telescope (Dataset ID 159)

## Features

The dataset contains 10 continuous features describing properties of the shower image:

| Feature    | Description                                                                  |
| ---------- | ---------------------------------------------------------------------------- |
| `fLength`  | Major axis of the ellipse                                                    |
| `fWidth`   | Minor axis of the ellipse                                                    |
| `fSize`    | Logarithm of the sum of the pixel contents                                   |
| `fConc`    | Ratio of the sum of the two highest pixels to `fSize`                        |
| `fConc1`   | Ratio of the highest pixel to `fSize`                                        |
| `fAsym`    | Distance from the highest pixel to the center, projected onto the major axis |
| `fM3Long`  | Third root of the third moment along the major axis                          |
| `fM3Trans` | Third root of the third moment along the minor axis                          |
| `fAlpha`   | Angle of the major axis with the vector to the origin                        |
| `fDist`    | Distance from the origin to the center of the ellipse                        |

The target variable is:

* `g` — Gamma-ray signal
* `h` — Hadron background

The UCI documentation notes that the class distribution is not representative of real observational data and that simple accuracy should therefore be interpreted carefully.

## Dataset Availability

The original dataset file (`magic04.data`) is **not included in this repository**.

This is intentional to keep the repository focused on the machine learning implementations and notebooks.

To reproduce the experiments, obtain the MAGIC Gamma Telescope dataset from the **UCI Machine Learning Repository** and place the dataset file in the project directory.

The UCI repository also provides access to the dataset through its official dataset page and the `ucimlrepo` Python package.

## 🛠️ Technologies Used

* Python
* Jupyter Notebook
* NumPy
* Pandas
* Matplotlib
* Scikit-learn

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd magic-gamma-telescope
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install numpy pandas matplotlib scikit-learn jupyter
```

### 4. Add the dataset

Download the MAGIC Gamma Telescope dataset from the UCI Machine Learning Repository and place the required data file in the project directory:

```text
magic-gamma-telescope/
├── magic04.data
├── magic-gamma-telescope-KNN.ipynb
├── ...
└── README.md
```

The dataset file is ignored by Git and will **not** be uploaded to GitHub.

### 5. Run the notebooks

Launch Jupyter:

```bash
jupyter notebook
```

Then open any of the model notebooks and run the cells.

## Reference

Bock, R. (2004). *MAGIC Gamma Telescope* [Dataset]. UCI Machine Learning Repository. DOI: **10.24432/C52C8B**.

The dataset is distributed by the UCI Machine Learning Repository under a **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.
