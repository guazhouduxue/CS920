# CS920 Lab 2 — Learning a linear digit classifier

This is a 50-minute MNIST lab. The score model is **S(x,j) = (Wx)_j**, with
W of shape (10, 784). Students learn W by minimising cross-entropy using
**full-batch gradient descent** and the explicitly supplied gradient
`(P - Y).T @ X / n`.

**No PyTorch, automatic differentiation, backpropagation, SGD or GPU is required
in the student notebook.** Only NumPy and Matplotlib are used.

## On a DCS lab desktop

1. Copy `lab2.ipynb` to `~/cs920/lab2/`.
2. Load the course module **before** activating the Lab 1 virtual environment:

    ```bash
    module load cs920-python
    cd ~/cs920
    source venv/bin/activate
    jupyter lab
    ```

3. In JupyterLab, open `lab2/lab2.ipynb` and run cells from top to bottom.
   Complete tasks A (linear scores), B (gradient), C (weight update).

If students have not yet created a venv, after loading the module they can
create one once from `~/cs920` using `python -m venv venv`.

