```
# Advanced Python

Python is a dynamically-typed language, meaning that variable types are set at runtime when a value is assigned to them.

For instance, consider this function:

```python
def fn(a, b):
    return a + b
```

The types of `a` and `b` aren't determined until values are assigned to them when the code runs. This allows code like

```python
fn("a", 1)
```

to execute without raising an exception until the function is actually called, resulting in an error if the types are incompatible:

```
>>> fn("a", 1)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
```

Even with Python 3’s type annotations, the language remains dynamically typed. These annotations provide the following benefits:

- **Code documentation**: Type annotations clarify expected variable types, making code easier to read and understand, which helps reduce bugs and speeds up development.
- **Linting and validation**: Code editors and CI pipelines can use these annotations to check types at build-time, catching potential bugs before production.
```
