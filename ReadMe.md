# NumPy — Complete Study Notes & Practice

A structured walkthrough of NumPy from fundamentals to advanced operations, built as part of my AI/ML engineering roadmap.

---

## Topics Covered

### 1. Array Basics
- Array creation: `np.array()`, `np.arange()`, `np.zeros()`, `np.ones()`, `np.linspace()`
- Properties: `shape`, `dtype`, `ndim`, `size`, `itemsize`
- Reshaping: `reshape()`, `ravel()`, `transpose()`

### 2. Indexing & Slicing
- Basic indexing and slicing
- **Fancy Indexing** — access multiple rows/columns at once
- **Boolean Indexing** — filter arrays using conditions
  ```python
  a[a > 50]                        # values greater than 50
  a[(a > 50) & (a % 2 == 0)]       # chained conditions
  ```

### 3. Broadcasting
- Operations between arrays of different shapes
- Broadcasting rules and error cases
- Practical examples: adding scalars, vectors to matrices

### 4. Math & Statistics
- `np.mean()`, `np.median()`, `np.std()`, `np.var()`
- `np.sum()`, `np.prod()`, `np.cumsum()`, `np.cumprod()`
- `np.percentile()`, `np.histogram()`, `np.corrcoef()`

### 5. Array Operations

| Function | Description |
|---|---|
| `np.sort(a, axis=)` | Sort along rows or columns |
| `np.append()` | Add elements or columns |
| `np.concatenate()` | Join arrays along an axis |
| `np.unique()` | Get distinct values |
| `np.expand_dims()` | Add a new axis |
| `np.flip()` | Reverse an array |
| `np.delete()` | Remove elements |
| `np.put()` | Replace values at specific indices |
| `np.clip()` | Clamp values between min and max |

### 6. Conditional Operations
```python
np.where(condition, true_value, false_value)
np.argmax(a, axis=)   # index of maximum value
np.argmin(a, axis=)   # index of minimum value
```

### 7. Set Operations
```python
np.union1d(a, b)      # all unique values from both
np.intersect1d(a, b)  # common values
np.setdiff1d(a, b)    # in a but not in b
np.setxor1d(a, b)     # in one but not both
np.isin(a, items)     # membership check
```

### 8. Missing Value Handling
```python
a[np.isnan(a)]    # get NaN positions
a[~np.isnan(a)]   # filter out NaN values
```

### 9. ML Math from Scratch
```python
# Sigmoid Function
def sigmoid(x):
    return 1 / (1 + np.exp(-x))

# Mean Squared Error
def mse(actual, predicted):
    return np.mean((actual - predicted) ** 2)
```

### 10. Speed & Memory Benchmarks
- Compared Python lists vs NumPy arrays for:
  - Computation speed (element-wise addition on 10M elements)
  - Memory usage (`sys.getsizeof`)
- **Result:** NumPy is significantly faster and more memory-efficient

---

## Key Takeaway

NumPy's power comes from **vectorized operations** — no loops, just math on entire arrays at once. This is the foundation of every ML framework (PyTorch, TensorFlow, scikit-learn).

---

## Tech Stack
- Python 3.x
- NumPy
- Matplotlib (for plotting graphs)

---

## Part of My AI/ML Roadmap
This repository is part of a structured 19-month roadmap to become an AI Engineer.

**Progress:** Phase 1 — Python & Scientific Stack (NumPy complete)

**Next:** Pandas → Matplotlib → EDA → Machine Learning
