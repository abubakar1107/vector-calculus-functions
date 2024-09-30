# README: Vector Calculus Operations with SymPy

## Overview

This Python script demonstrates how to compute key vector calculus operations—gradient, divergence, curl, and Laplacian—using symbolic computation in the `SymPy` library. These operations are widely used in physics and engineering, particularly in fields such as electromagnetism, fluid dynamics, and potential theory.

### Key Components
The script includes functions to calculate:
1. **Gradient of a scalar function**
2. **Divergence of a vector field**
3. **Curl of a vector field**
4. **Laplacian of a scalar field**
5. **Laplacian of a vector field**

The script uses symbolic variables for mathematical expressions and leverages SymPy’s differentiation capabilities to compute the desired quantities.

### Dependencies
- **SymPy**: This is a Python library for symbolic mathematics. You can install it using `pip`:
  ```bash
  pip install sympy
  ```
- **NumPy**: This script imports `numpy` but does not explicitly use it in the current implementation. You can remove the import or install NumPy using:
  ```bash
  pip install numpy
  ```

### Symbol Definitions

The following symbolic variables are defined at the beginning of the script:
- `x, y, z`: Coordinates for scalar and vector fields in a 3D Cartesian space.
- `i, j, k`: Unit vectors along the `x`, `y`, and `z` axes, respectively.

### Function Descriptions

#### 1. `grad(func)`
This function computes the gradient of a scalar function `func`. The gradient is a vector field representing the rate and direction of the fastest increase of the scalar function.

- **Input**: Scalar function `func`
- **Output**: Gradient vector in terms of `i`, `j`, and `k`

#### 2. `diver(ls)`
This function computes the divergence of a vector field `ls`. The divergence gives a scalar measure of the net flux per unit volume at a point in a vector field.

- **Input**: Vector field `ls` (a list of three scalar expressions corresponding to the `x`, `y`, and `z` components of the vector field)
- **Output**: Scalar divergence

#### 3. `curl(ls)`
This function computes the curl of a vector field `ls`. The curl gives the amount of rotation or the tendency of a vector field to circulate around a point.

- **Input**: Vector field `ls`
- **Output**: Curl vector in terms of `i`, `j`, and `k`

#### 4. `laplace_scalar(fun)`
This function computes the Laplacian of a scalar function `fun`. The Laplacian is a measure of the rate at which the average value of the function around a point differs from its value at that point.

- **Input**: Scalar function `fun`
- **Output**: Scalar Laplacian

#### 5. `laplace_vector(ls)`
This function computes the Laplacian of a vector field `ls`. It applies the Laplacian operator to each component of the vector field.

- **Input**: Vector field `ls`
- **Output**: Vector Laplacian

### Example Usage

Below are examples of how to use the functions defined in the script.

#### 1. Gradient of a Scalar Function
```python
g = log(x**2 + y**2 + z**2)
grad_g = grad(g)
print(grad_g)
```

#### 2. Divergence of a Vector Field
```python
fg = [x**2 - y**2, 2*x*y, y**2 - x*y]
div_fg = diver(fg)
print(div_fg)
```

#### 3. Curl of a Vector Field
```python
curl_fg = curl(fg)
print(curl_fg)
```

#### 4. Laplacian of a Scalar Function
```python
fn = (x**2) * (y**3) * (z**2)
lap_fn = laplace_scalar(fn)
print(lap_fn)
```

#### 5. Laplacian of a Vector Field
```python
lap_fg = laplace_vector(fg)
print(lap_fg)
```

### Conclusion

This script provides reusable functions to compute gradient, divergence, curl, and Laplacian in symbolic form using SymPy. These operations are essential tools in vector calculus, making the script useful for applications in physics, engineering, and mathematics.
