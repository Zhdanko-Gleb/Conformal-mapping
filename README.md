# Conformal Mapping
## Description

This project provides a Python-based implementation of the **Joukowsky conformal mapping**. The primary goal is to facilitate the transformation of complex shapes, particularly for use in **Computational Fluid Dynamics (CFD)** simulations. Conformal mapping is a powerful technique in both theoretical and applied mathematics, and this project focuses on its practical applications—such as the optimization of wing designs for wind farming and aerodynamics.

## Key Features
- **Joukowsky Transformation**: Simplifies the analysis of flow around airfoils by mapping a circular region into an airfoil shape.
- **Customization Parameters**: Offers flexible control over shape and curvature using various parameters.
- **Practical Applications**: Ideal for use in CFD to simulate airflow and optimize wing design.

## Parameters

This project uses several key parameters to control the Joukowsky transformation and shape generation:

- `a`: Horizontal shift of the circle. Positive values shift the circle to the left. This parameter also affects the vertical scaling of the wing. A larger absolute value (up to the radius) makes the shape more circular.
- `b`: Vertical shift of the circle. Positive values shift the circle upwards. This parameter controls the cambering of the wing, with larger values resulting in a more curved shape.
- `r`: Radius of the circle to be transformed.
- `r_max`: Maximum radius of the grid to represent.
- `rad_steps`: Number of divisions in the radial direction for the grid.
- `phi_steps`: Number of divisions in the angular direction for the grid.

## Insights

- **`a` Parameter (Vertical Scaling)**: The value of `a` determines how much the resulting wing deviates from a perfect circle. Larger values (up to the circle’s radius) make the wing shape rounder, while smaller values stretch it more vertically.
  
- **`b` Parameter (Cambering)**: The value of `b` controls the curvature or camber of the wing. Higher values increase the curvature, allowing for the design of wings with more pronounced aerodynamic profiles.

These parameters allow fine-tuning of wing shapes, offering flexibility to adapt designs for specific applications such as energy-efficient wind turbine blades or optimized aircraft wings.
![Conformal Mapping Visualization](https://github.com/Zhdanko-Gleb/Conformal-mapping/blob/main/images/output.png)


## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Zhdanko-Gleb/Conformal-mapping.git
   ```

2. Navigate into the project directory:
   ```bash
   cd Conformal-mapping
   ```

3. (Optional) Create and activate a virtual environment:
   ```bash
   python3 -m venv env
   source env/bin/activate  # On Windows use `env\Scripts\activate`
   ```

4. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

After installing the project, you can apply the conformal mapping transformation by importing the module and using the functions in your Python code. Here's a basic example of how to use it:

```python
from conformal_mapping import joukowsky_map

# Define parameters
a = 0.1
b = 0.05
r = 1.0
r_max = 5.0
rad_steps = 100
phi_steps = 200

# Apply Joukowsky conformal mapping
wing_shape = joukowsky_map(a, b, r, r_max, rad_steps, phi_steps)

# Output the mapped shape
print(wing_shape)
```

To visualize the results, you can use the accompanying Jupyter Notebooks or integrate this into your CFD pipeline for further analysis.

## Contributing

Contributions are welcome! If you have ideas for improvements or new features, please follow these steps:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some amazing feature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

For detailed guidelines, check the `CONTRIBUTING.md` file.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Credits

- **Zhdanko Gleb**: Author and main contributor of the project.
