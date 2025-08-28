Derivation of the Heat Equation Solution Using Separation of Variables
We solve the one-dimensional heat equation:

$$\frac{\partial u}{\partial t} = k \frac{\partial^2 u}{\partial x^2},$$

with initial condition $u(x,0) = f(x)$, and boundary conditions $u(0,t) = u(L,t) = 0$, where $L$ is the length of the rod and $k$ is the thermal diffusivity.
Separation of Variables
Assume a solution of the form:
$$ u(x,t) = X(x)T(t). $$
Substitute into the heat equation:
$$ X(x)T'(t) = k X''(x)T(t). $$
Divide through by $X(x)T(t)$ (assuming $X(x)T(t) \neq 0$):
$$ \frac{T'(t)}{k T(t)} = \frac{X''(x)}{X(x)}. $$
Since the left side depends only on $t$ and the right side only on $x$, both must equal a constant, say $-\lambda$:
$$ \frac{T'(t)}{k T(t)} = \frac{X''(x)}{X(x)} = -\lambda. $$
This gives two ordinary differential equations (ODEs):

Spatial ODE: $$ X''(x) + \lambda X(x) = 0, $$
Temporal ODE: $$ T'(t) + \lambda k T(t) = 0. $$

The negative sign for $\lambda$ is chosen for convenience, as the boundary conditions suggest positive eigenvalues.
Applying Boundary Conditions
The boundary conditions are:
$$ u(0,t) = X(0)T(t) = 0, \quad u(L,t) = X(L)T(t) = 0. $$
Since $T(t) \neq 0$ (to avoid the trivial solution), we have:
$$ X(0) = 0, \quad X(L) = 0. $$
Solving the Spatial ODE
The spatial ODE is:
$$ X''(x) + \lambda X(x) = 0. $$
The general solution is:
$$ X(x) = A \cos(\sqrt{\lambda} x) + B \sin(\sqrt{\lambda} x). $$
Apply the boundary condition at $x = 0$:
$$ X(0) = A \cos(0) + B \sin(0) = A = 0 \implies A = 0. $$
Thus:
$$ X(x) = B \sin(\sqrt{\lambda} x). $$
Apply the boundary condition at $x = L$:
$$ X(L) = B \sin(\sqrt{\lambda} L) = 0. $$
For non-trivial solutions ($B \neq 0$):
$$ \sin(\sqrt{\lambda} L) = 0 \implies \sqrt{\lambda} L = n \pi, \quad n = 1, 2, 3, \dots, $$
$$ \lambda_n = \left( \frac{n \pi}{L} \right)^2. $$
The eigenfunctions are:
$$ X_n(x) = B_n \sin\left( \frac{n \pi x}{L} \right). $$
Solving the Temporal ODE
The temporal ODE is:
$$ T'(t) + \lambda k T(t) = 0 \implies T'(t) = -\lambda k T(t). $$
The solution is:
$$ T(t) = C e^{-\lambda k t}. $$
Using $\lambda_n = \left( \frac{n \pi}{L} \right)^2$:
$$ T_n(t) = C_n e^{-\left( \frac{n \pi}{L} \right)^2 k t}. $$
Forming the General Solution
The solution for each $n$ is:
$$ u_n(x,t) = X_n(x)T_n(t) = A_n \sin\left( \frac{n \pi x}{L} \right) e^{-\left( \frac{n \pi}{L} \right)^2 k t}, $$
where $A_n = B_n C_n$. The general solution is a linear combination:
$$ u(x,t) = \sum_{n=1}^\infty A_n \sin\left( \frac{n \pi x}{L} \right) e^{-\left( \frac{n \pi}{L} \right)^2 k t}. $$
Satisfying the Initial Condition
To satisfy $u(x,0) = f(x)$:
$$ u(x,0) = \sum_{n=1}^\infty A_n \sin\left( \frac{n \pi x}{L} \right) = f(x). $$
This is a Fourier sine series. To find $A_n$, use the orthogonality of the sine functions:
$$ \int_0^L \sin\left( \frac{m \pi x}{L} \right) \sin\left( \frac{n \pi x}{L} \right) dx = \begin{cases}\frac{L}{2} & \text{if } m = n, \0 & \text{if } m \neq n.\end{cases} $$
Multiply both sides of the initial condition by $\sin\left( \frac{m \pi x}{L} \right)$ and integrate:
$$ \int_0^L f(x) \sin\left( \frac{m \pi x}{L} \right) dx = \sum_{n=1}^\infty A_n \int_0^L \sin\left( \frac{n \pi x}{L} \right) \sin\left( \frac{m \pi x}{L} \right) dx = A_m \frac{L}{2}. $$
Thus:
$$ A_n = \frac{2}{L} \int_0^L f(x) \sin\left( \frac{n \pi x}{L} \right) dx. $$
Final Solution
The solution to the heat equation is:
$$ u(x,t) = \sum_{n=1}^\infty A_n \sin\left( \frac{n \pi x}{L} \right) e^{-\left( \frac{n \pi}{L} \right)^2 k t}, $$
where:
$$ A_n = \frac{2}{L} \int_0^L f(x) \sin\left( \frac{n \pi x}{L} \right) dx. $$
