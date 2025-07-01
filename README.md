# COMP0086 — Probabilistic & Unsupervised Learning • Coursework
MSc in Machine Learning, University College London (2024 / 25)

This repository contains the COMP0086 Probabilistic and Unsupervised Learning coursework.

The questions can be found here: https://www.gatsby.ucl.ac.uk/teaching/courses/ml1/COMP0086-summative.pdf

| Path       | Description                                                                                            |
| ---------- | ------------------------------------------------------------------------------------------------------ |
| `main.tex` | LaTeX source of the written report.                                  |
| `requirements.txt` | Requirememts to run the code.                                  |
| `README.md` | Readme file detailing the project.                                  |
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

## Coursework Overview  

**Exercise 1 – Binary-vector models** 

- **Multivariate Bernoulli fitting** — derived closed-form ML and MAP estimators for every pixel of the 8 × 8 digit images and visualised both parameter vectors as images.  
- **Why not Gaussians?** — explained the unsuitability of a multivariate normal for binary data.

**Exercise 2 – Model selection**

- Computed marginal likelihoods (under uniform Beta priors) for three nested Bernoulli models:  
  1. fixed $p_d = 0.5$; 2. shared unknown $p$; 3. independent unknown $p_d$.  
- Returned posterior probabilities and discussed Occam’s razor effect.

**Exercise 3 – EM for mixtures of Bernoullis**

- **E-step**: derived responsibilities $r_{nk}$ for K-component mixture.  
- **M-step**: produced updates for mixing weights and pixel probabilities.  
- **Implementation**: custom EM routine with log-likelihood convergence plots for $K \in \{2,3,4,7,10\}$; displayed component means as 8 × 8 images; analysed sensitivity to initialisation.  
- Bonus discussion (bits-per-pixel vs gzip) included.

**Exercise 4 – LGSSM, Kalman & EM**

- Ran provided Kalman filter / smoother on spinning-top time-series; plotted filtered and smoothed states plus log-det covariances, commenting on their divergence/convergence behaviour.  -
- Full EM re-estimation was outlined but only the Kalman diagnostic plots were delivered (6 / 35). 

**Exercise 5 – Deciphering text with MCMC**  

- Trained a bigram language model on *War & Peace* to obtain $ϕ,ψ$.  
- Implemented Metropolis–Hastings sampler over 53-symbol permutations with random swap proposals; reported the first 60 decrypted characters every 100 iterations and analysed ergodicity when some transition counts are zero.

**Exercise 6 – Gibbs sampling for LDA** 

- **Not attempted** – left for future work.

**Exercise 7 – Optimisation miscellany** 

- **Constrained extremum** — used Lagrange multipliers to locate two stationary points of $f(x,y)=x+2y$ under $y^{2}+xy=1$.  
- **Newton for $\ln a$** — framed $f(x)=e^{x}-a$; derived update $x_{n+1}=x_{n}-(e^{x_{n}}-a)/e^{x_{n}}$.

**Eigenvalues as an optimisation problem**

- Proved that maximising the Rayleigh quotient over the sphere yields the largest eigenvalue; supplied two proofs (extreme-value theorem and spectral decomposition) and showed non-maximisation for vectors outside the leading eigenspace.


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
UCL-COMP0086-Probabilistic-Unsupervised-Learning-Coursework/
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

