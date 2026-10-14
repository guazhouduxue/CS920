# CS920 — Lab 1: Can we trust a good fit?

**Duration:** 50 minutes (including initial log-in and JupyterLab familiarisation).

## Before the lab (instructor)

Copy these **three student files** into the DCS course directory,
`/modules/cs920/lab1/`:

- `lab1.ipynb`
- `lab1_data.npz`
- `lab1_reveal.npz`

Keep `lab1_solutions.ipynb` and `instructor_notes.md` private.
The notebooks work offline with the centrally installed `cs920-python` module.
No GPU is needed for Lab 1.

## Students: first session on a DCS lab desktop

In a terminal, run:

```bash
module load cs920-python
mkdir -p ~/cs920/lab1
cp /modules/cs920/lab1/lab1.ipynb /modules/cs920/lab1/lab1_*.npz ~/cs920/lab1/
cd ~/cs920
python -m venv venv           # only if this environment has not been created
source venv/bin/activate
jupyter lab
```

Open `lab1/lab1.ipynb` in JupyterLab. Press **Shift+Enter** to execute cells.
If Firefox does not open automatically, use the local URL printed in the terminal.

### For later sessions

```bash
module load cs920-python
cd ~/cs920
source venv/bin/activate
jupyter lab
```

## Troubleshooting

- `No module named ...`: check that `module load cs920-python` was run **before** activating `venv`.
- `FileNotFoundError: lab1_data.npz`: keep the notebook and both `.npz` files together in `~/cs920/lab1/`.
- `...` placeholders cause an error: replace the task-A/task-B `...` with working Python code, then rerun the cell.
- No browser window: paste the `http://localhost:...` Jupyter URL into Firefox.
- GPU errors: Lab 1 is CPU-only; no GPU should be used.

### What the notebook asks students to code

1. Polynomial least squares with `np.vander` and `np.linalg.lstsq` (2 lines).
2. Mean squared error with NumPy (1 line).

The notebook begins with the energy
$E_{v,\phi}(x,y)=(\langle v,\phi(x)\rangle-y)^2$ for a *specified* feature map
$\phi:\mathbb R\to\mathbb R^d$ and weights $v\in\mathbb R^d$.
The per-example loss is chosen to equal this energy. During Lab 1, **the feature
map is fixed and only $v$ is learnt**; different preset polynomial maps are
compared using validation data. Later labs will learn the feature map too.
A polynomial of degree $k$ uses $\phi_k(x)=(1,x,\ldots,x^k)$, with
$d=k+1$. The rest of the lab is plotting, comparing errors and interpreting
training versus generalisation.
