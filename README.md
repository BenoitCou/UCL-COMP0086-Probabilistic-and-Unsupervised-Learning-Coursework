# COMP0086 — Probabilistic & Unsupervised Learning • Coursework
MSc in Machine Learning, University College London (2024 / 25)

This repository contains the COMP0086 Probabilistic and Unsupervised Learning coursework.

The questions can be found here: https://www.gatsby.ucl.ac.uk/teaching/courses/ml1/COMP0086-summative.pdf

| Path       | Description                                                                                            |
| ---------- | ------------------------------------------------------------------------------------------------------ |
| `main.tex` | LaTeX source of the written report.                                  |
| `images/`  | Auxiliary figures referenced by `main.tex`.                                                            |
| `code/`    | All PJupyter notebooks with the data files needed to reproduce the experiments. |

## Quick-start

```bash
# 1. Clone the repo
git clone https://github.com/BenoitCou/UCL-COMP0086-Probabilistic-Unsupervised-Learning-Coursework
cd UCL-COMP0086-Probabilistic-Unsupervised-Learning-Coursework

# 2. Create & activate a virtual environment
python -m venv .venv

# 3. Install Python dependencies
pip install -r requirements.txt

# 4. Launch the notebooks
jupyter notebook code/
```

## Compiling the report
```bash
latexmk -pdf main.tex
```

## Marks obtained

**Grade**: 100/100

| Question | Score   | Comments (lecturer’s feedback)                                                                                                                                    |
| -------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Q1       | 22 / 25 | (a–d) good work. (e) −3 : does not explain why MAP may be better or worse than MLE.                                                                               |
| Q2       | 15 / 15 | Great work.                                                                                                                                                       |
| Q3       | 66 / 70 | Strong answers overall. Minor issues: (e) BIC / Prior / k-means initialisation not fully discussed; (f) link to compression missing; (g) lacks concrete examples. |
| Q4       | 6 / 35  | (a) good, but initial boundary spikes of log det (V) should point up; (b) only wrote Cₙₑw & Aₙₑw (1 / 25); (c) not attempted.                                     |
| Q5       | 70 / 70 | Excellent. Note: zero transition probabilities do **not** necessarily break irreducibility unless two states have no connecting path.                             |
| Q6       | 0 / 60  | Not attempted.                                                                                                                                                    |
| Q7       | 14 / 15 | (a) good; (b) −1 : sign error in update rule.                                                                                                                     |
| Q8       | 19 / 20 | (c) could show a few more intermediate steps deriving R\_A(x) < λ₁.                                                                                               |

## Repo Structure

```kotlin
UCL-COMP0086-Probabilistic-Unsupervised-Learning/
├── code/
│   ├── Code_ex1_ex2_ex3.ipynb
│   ├── Code_ex4.ipynb
│   ├── Code_ex5.ipynb
│   ├── binarydigits.txt
│   ├── message.txt
│   ├── ssm_spins.txt
│   ├── symbols.txt
│   └── war_and_peace.txt
├── images/
│   └── ...
├── main.tex
└── requirements.txt
```

