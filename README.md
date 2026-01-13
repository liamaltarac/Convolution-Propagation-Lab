# Convolution Propagation Lab

An interactive browser-based sandbox to explore how repeated convolution and activation functions affect signal propagation in image space. This tool allows you to experiment with different kernels, activation functions, and boundary conditions to observe their impact on signal evolution.

## Features

- **Interactive Viewer**: Visualize signal propagation as a heatmap.
- **Customizable Kernels**: Edit or paste kernel matrices (3×3 or 5×5).
- **Pattern Selection**: Choose from predefined input patterns like impulse, lines, squares, and noise.
- **Activation Functions**: Switch between Identity, ReLU, and tanh.
- **Boundary Handling**: Experiment with zero padding, wrap, or reflect modes.
- **Normalization Options**: Per-step standardization or scaling.
- **GIF Export**: Save the simulation as an animated GIF.

## How to Use

1. Open `index.html` in a modern browser (no server required).
2. Use the **Controls** panel to:
   - Select a pattern and kernel preset.
   - Adjust grid size, steps, and playback FPS.
   - Choose activation functions and boundary conditions.
3. Click **Simulate** to generate the propagation.
4. Use **Play**, **Pause**, or **Step** to control the animation.
5. Export the simulation as a GIF using the **Export GIF** button.

## Core Equation

The simulation is based on the following update rule:

x(t+1) = act(conv(x(t), W))

Where:
- `x(t)` is the signal at time `t`.
- `W` is the convolution kernel.
- `act` is the activation function.

## What to Observe

- **Diffusion vs Transport**: Does energy spread symmetrically or drift?
- **Stability**: Does the signal explode, vanish, or converge?
- **Nonlinearity Bias**: How does ReLU affect propagation compared to Identity?
- **Boundary Effects**: Compare zero padding, wrap, and reflect modes.

## Notes

This tool is a simplified single-channel model designed for intuition. It does not replicate full CNN training dynamics but helps visualize how kernel structure and nonlinearities shape signal flow over repeated layers.

## Built With

- **HTML5 Canvas**: For rendering the simulation.
- **Bootstrap 5**: For responsive UI components.
- **gif.js**: For client-side GIF encoding.

## License

This project is open-source and available under the [MIT License](LICENSE).
