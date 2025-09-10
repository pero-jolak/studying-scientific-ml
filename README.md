# A learning process of Scientific Machine Learning (SciML)

In this repository I share my learning process of scientific machine learning.

## Numerical linear algebra

In this part I implement two iterative methods for solving large, sparse systems of linear equations which are typically encountered in solving engineering problems involving partial differential equations.

### Conjugate gradient method (CG)

- [Basics](https://github.com/pero-jolak/studying-scientific-ml/blob/main/Numerical%20linear%20algebra/Conjugate%20gradient%20method/Conjugate%20gradient%20method.pdf) of the conjugate gradient method.
- [Python implementation](https://github.com/pero-jolak/studying-scientific-ml/blob/main/Numerical%20linear%20algebra/Conjugate%20gradient%20method/conjugate_gradient_method.ipynb) of the CG method from scratch, compared at the end with the SciPy implementation.

### Generalized minimal residual method (GMRES)

- [Basics]([https://github.com/pero-jolak/studying-scientific-ml/blob/main/Numerical%20linear%20algebra/Conjugate%20gradient%20method/Conjugate%20gradient%20method.pdf](https://github.com/pero-jolak/studying-scientific-ml/blob/main/Numerical%20linear%20algebra/Generalized%20minimal%20residual%20method/gmres.pdf)) of the GMRES algorithm.
- [Python implementation]([https://github.com/pero-jolak/studying-scientific-ml/blob/main/Numerical%20linear%20algebra/Conjugate%20gradient%20method/conjugate_gradient_method.ipynb](https://github.com/pero-jolak/studying-scientific-ml/blob/main/Numerical%20linear%20algebra/Generalized%20minimal%20residual%20method/gmres_implementation.ipynb)) of the GMRES method from scratch with restarts. At the end, a SciPy implementation is called to verify the results.

## Partial differential equations (PDEs)

In order to build stronger understanding, for each PDE I do the following:

- Derive solution(s) to a particular PDE with a known method (separation of variables, Fourier transform, Laplace transform, etc.);
- Use a numerical algorithm (Finite difference or Finite element) to approximate the solution.
- Use a modern technique (Physics-informed Neural Networks or operator based method).

### Heat equation

Solving the 1-D Heat equation:
- Analytically: [separation of variables](https://github.com/pero-jolak/studying-scientific-ml/blob/main/Partial%20differential%20equations%20(PDEs)/Heat%20equation/heat_eq_analytic.pdf) and Fourier transform.
- Numerically: [Derivation](https://github.com/pero-jolak/studying-scientific-ml/blob/main/Partial%20differential%20equations%20(PDEs)/Heat%20equation/Crank-Nicolson-derivation.pdf) of Crank-Nicolson finite difference method and [Python implementation](https://github.com/pero-jolak/studying-scientific-ml/blob/main/Partial%20differential%20equations%20(PDEs)/Heat%20equation/heat_equation_crank_nicolson.ipynb).
- Physics-informed neural network (PINN):
  - [Classic PINN](https://github.com/pero-jolak/studying-scientific-ml/blob/main/Partial%20differential%20equations%20(PDEs)/Heat%20equation/pinn_heat_equation.ipynb) (with residual loss and data loss from BCs and ICs)

### Laplace's equation

### Poisson's equation

### Wave equation

## Neural ODEs

## Neural SDEs

## Operator learning

## Sparse identification of non-linear dynamics (SINDy)


## Resources

### PDEs:

-  
