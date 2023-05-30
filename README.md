# Bidimensional-FirstOrder-Dynamical-Systems

This repository provides Python code for solving systems of ordinary differential equations (ODEs) symbolically and numerically, using the symbolic computation library `SymPy` and the numerical computation library `SciPy`. The code includes a numerical implementation designed to handle systems of ODEs expressed in matrix form, enabling an analysis of their properties through the determinant, eigenvalues, and eigenvectors. It provides a framework to study autonomous and homogeneous systems of ODEs.

## **Symbolic Implementation**

### *Code using SymPy to solve the ODEs analytically*

This section code uses the `SymPy` package to solve the system of equations dx/dt = ax + by and dy/dt = cx + dy analytically. I structured the code into the following functions to define and solve these equations, find their fixed points, and plot the solutions.

- `solve_odes`: This function takes as input the coefficients `a, b, c, d` of the system of ODEs and returns the solutions.

- `find_fixed_points`: This function takes as input the coefficients `a, b, c, d` and returns the fixed points.

- `solve_initial_conditions`: This function takes the solution of the system of ODEs and initial conditions for `x` and `y`, along with the values of coefficients `a, b, c, d`. It solves the system for the integration constants in the solution using the initial conditions.

- `plot_results_linear`: This function takes the values of time, `x` and `y` solution, initial conditions, fixed points, and coefficients to plot the time evolution of `x` and `y`, a phase plane with the orbit of the system, the initial conditions, and the fixed points.

- `plot_3D_trajectory`: This function takes the `x` and `y` solution values and the time points to plot the 3D trajectory of the system.

The `main` function calls the above ones to solve the system of ODEs for given coefficient and initial condition values, find the fixed points, plot the solutions, and the 3D trajectory. Finally, there is an additional section to verify the analytical solutions obtained.

## **Numerical Implementation**

The numerical implementation uses `SciPy` to solve the ODEs numerically. There is an option analogous to the symbolic and another using matrix notation.

### *Code using SciPy to solve the ODEs numerically*

This section of the code provides functions to solve the system numerically. This section code presents the definitions of the following functions:

- `system` and `equations:`  These functions define the ODEs as (dxdt = a*x + b*y, dydt = c*x + d*y), and (eq1 = a*x + b*y, eq2 = c*x + d*y) with different input parameters for using with distinct built-in functions.

- `solve_odes_Num:` This function numerically solves the ODEs using the initial state and given parameters `a, b, c, and d`.

- `find_fixed_points_Num:` This function finds the fixed points by applying the Newton-Raphson method using the `fsolve` function from `SciPy`.

- `plot_results_linear:` This function plots the time evolution of the system and the phase plane, including the initial condition, the fixed point, and the vector field.

- `plot_3D_trajectory:` This function creates a 3D plot of the trajectory over time.

The `main` function sets the initial conditions and parameters, solves the ODEs, finds the fixed points, and finally calls the functions to plot the results and the 3D trajectory.

### *Code using SciPy to solve the ODEs numerically using matrix notation*

This section of the code provides functions to solve a system of ODEs numerically using matrix notation. The system is solved using the `odeint` function from `SciPy`. This section code presents the definitions of the following functions:

- `system` and `equations:`  These functions define the system of ODEs as a dot product of matrix A and the state vector with different input parameters for use with distinct built-in functions.

- `solve_odes_Num:` This function numerically solves the ODEs using the initial state and matrix A.

- `find_fixed_points_Num:` This function finds the fixed points.

- `system_properties:` This function calculates the determinant,  eigenvalues, and eigenvectors and relates to the stability and uniqueness of the solution.

- `plot_results_linear:` This function plots the system time evolution and the phase plane, including the initial condition, the fixed point, and the vector field.

- `plot_3D_trajectory:` Similar to the first part, this function plots the 3D trajectory over time.

The `main` function chooses over different sets of parameters representing the cases of real and complex eigenvalues, solves the ODEs, finds the fixed points, and plots the results and the 3D trajectory.

## Prerequisites

The following Python libraries are needed to run the code:

- NumPy (`linspace`, `sqrt`, `meshgrid`, ...)
- SymPy (`symbols`, `Function`, `Eq`, `dsolve`, `solve`, `lambdify`, `diff`, `simplify`)
- Matplotlib (`pyplot.quiver`, ...)
- SciPy (`odeint`, `fsolve`)

## Usage

To use this repository, you can clone it locally or open the notebook directly in Google Colab from the Github repository.

## Contribute

If you have any suggestions, improvements, or bug fixes, please feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
