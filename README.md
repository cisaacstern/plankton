# plankton

To clone this project to your local machine, run:

```
➜ git clone https://github.com/cisaacstern/plankton.git && cd plankton
```
> **Note:** `&&` is used to chain two shell commands together. These commands could also be run one-at-a-time.

You will now be inside the project's top-level directory, which contains an `environment.yml` file defining a project-specific `conda` environment named `plankton`. To build and activate it, run:

```
➜ conda env create --file environment.yml && conda activate plankton
```

With the `plankton` environment activated, you can now enter the `ipython` interpreter:

```
➜ ipython
```

> **Note:** To exit the interpreter at any time, use `Ctrl+D`.

In the interpreter, we will try out our functions. To start, import numpy along with our custom module, `plankton.py`, as follows:

```python
In [1]: import numpy as np

In [2]: import plankton
```
Our custom function, `calculate_flor` takes a numpy array as input, so we'll define one here:

```python
In [3]: ocean_array = np.array([4.5, 2.1, 0.2])
```
Now that we have an input defined, we can pass it to our custom function:

```python
In [4]: plankton.calculate_flor(array=ocean_array)
Out[4]: array([14.460552 ,  6.7482576,  0.6426912])
```

The output array is the result of each value in the array being multiplied by the `PLANKTON_CONSTANT`, which we defined in `plankton.py`. To remind ourselves what this value is, we can ask for it:

```python
In [5]: plankton.PLANKTON_CONSTANT
Out[5]: 3.213456
```

If we wanted to reuse our fluorescence array as input for some downstream functions, we could assign it to a new variable:

```python
fluorescence = plankton.calculate_flor(array=ocean_array)
```
