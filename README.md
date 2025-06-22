# `asvector`: vectorize your Python functions

This project is a minimalist PoC that aims to "natively" vectorize Python function, similarly to what R does.

```python
from asvector import vectorize

@vectorize
def add(a, b):
    return a + b

@vectorize
def concat(a, b):
    return f"{a}-{b}"
```

```py
>>> add(1, 2)
3

>>> add([1, 2, 3], 10)
[11, 12, 13]

>>> add([1, 2], [10, 20])
[11, 22]

>>> concat("x", "a")
x-a

>>> concat("x", ["a", "b", "c"])
['x-a', 'x-b', 'x-c']
```

<br>

You can try it:

```bash
pip install git+https://github.com/JosephBARBIERDARNAL/asvector.git
```
