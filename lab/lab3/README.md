# CS920 Lab 3 — Learning nonlinear representations (Week 4)

**Duration:** 50 minutes. **Requirements:** standard `cs920-python` module (PyTorch, NumPy, Matplotlib, scikit-learn and JupyterLab). **GPU:** not required. **Data:** generated in notebook; no downloads.

## Student setup (DCS lab desktop)

```bash
module load cs920-python
cd ~/cs920
source venv/bin/activate
mkdir -p lab3
cp /modules/cs920/labs/lab3/lab3.ipynb ~/cs920/lab3/
cd ~/cs920/lab3
jupyter lab
```

If the `~/cs920/venv` environment has not yet been created, create it as instructed in Lab 1 *after* loading the `cs920-python` module. Run cells in order with Shift+Enter. There are three short TODOs in the student notebook, all accompanied by guidance; an optional final section removes ReLU.

## Instructor staging

Distribute only `lab3.ipynb` in `/modules/cs920/labs/lab3/` and ensure the parent directories are accessible to students. Keep `lab3_instructor.ipynb` in an instructor-only location. Students should **copy** the notebook to `~/cs920/lab3` so that they can save their edits.

The notebooks were written to run on CPU and use a fixed `make_moons` seed and train/validation split. They don't depend on network access, extra datasets or a GPU reservation.
