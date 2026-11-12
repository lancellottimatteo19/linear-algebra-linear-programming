# Linear Algebra and Linear Programming

Core numerical methods behind optimisation and regression: singular value decomposition, least squares and
constrained linear programming, implemented from first principles and checked against library solvers.

## Contents — [`linear_algebra_and_linear_programming.ipynb`](linear_algebra_and_linear_programming.ipynb)

* Singular value decomposition (**SVD**, $A = U \Sigma V^T$): exact reconstruction and the condition number.
* **Least squares** on noisy data through the pseudo-inverse $x = V \Sigma^{-1} U^T b$, compared with
  `np.linalg.lstsq`.
* **Linear programming** with `scipy.optimize.linprog` (HiGHS): maximise $Z = 3x_0 + 5x_1$ subject to
  $x_0 + 2x_1 \le 8$ and $4x_0 + 2x_1 \le 16$.
* A chart of the **feasible region**, the iso-profit line and the optimal vertex.

## Results

* Fitted line: intercept 1.1289 and slope 2.3840 (true values 1.0 and 2.5). The SVD solution matches `lstsq`, and
  the condition number is 11.69.
* The linear programme is optimal at $(x_0, x_1) = (8/3, 8/3)$ with $Z = 64/3 \approx 21.33$, the vertex where the
  two constraints meet.

## How to run

Requires Python 3.9 or later.

```bash
git clone https://github.com/lancellottimatteo19/linear-algebra-linear-programming.git
cd linear-algebra-linear-programming
pip install -r requirements.txt
jupyter lab
```

The notebook is saved with its outputs, so charts and results are visible directly on GitHub.
