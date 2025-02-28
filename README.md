# ProjectileMotionVisualizer

## Overview
The **ProjectileMotionVisualizer** is a MATLAB App designed to simulate the trajectory of a projectile under the influence of gravity. It supports simulations for various celestial bodies—including the Sun, Mercury, Venus, Earth, Mars, Jupiter, Saturn, Uranus, Neptune, and the Moon—as well as a custom gravitational setting.

## Features
- **Multi-Planet Support:** Choose from preset gravitational accelerations for different planets and the Sun.
- **Custom Gravity Option:** Enable custom gravitational acceleration by selecting the "Custom" option.
- **Dynamic Simulation:** Input initial speed, launch angle, and starting positions (X, Y) to compute and plot the projectile's trajectory.
- **Visual Annotations:** 
  - A red marker highlights the maximum height with a label displaying the height and horizontal distance.
  - A green marker indicates the landing point (range) with an associated label.
- **Hold-On Mode:** Option to retain previous trajectories on the plot.
- **Reset Functionality:** Quickly clear the plot and restore default settings.

## Prerequisites
- MATLAB (R2018a or later recommended) with App Designer support.

## Installation
1. **Download/Clone:** Obtain the source code from your repository.
2. **Open in MATLAB:** Navigate to the project folder and open the `ProjectileMotionVisualizer.mlapp` file using MATLAB App Designer.

## Usage
1. **Launch the App:**  
   Run the app by clicking the **Run** button in App Designer or by typing `ProjectileMotionVisualizer` in the MATLAB Command Window.

2. **Set Simulation Parameters:**  
   - **Initial Speed:** Enter the projectile's initial speed (m/s) in the "Starting speed" field.
   - **Launch Angle:** Set the launch angle (°) in the "Throwing angle" field.
   - **Initial Position:** Specify the starting X and Y coordinates in the "Starting X" and "Starting Y" fields, respectively.

3. **Select Gravitational Setting:**  
   - **Preset Options:** Click one of the planetary buttons (e.g., *Sun*, *Mercury*, *Earth*, etc.) to use the predefined gravitational acceleration.
   - **Custom Gravity:** Select the **Custom** button to enable the gravity input field and provide your own gravitational acceleration value.

4. **Simulate:**  
   Press the **Simulate** button to compute and display the projectile's trajectory on the plot (UIAxes).  
   - The trajectory will include markers for the maximum height and the landing point with corresponding annotations.

5. **Hold-On Mode:**  
   Toggle the **Hold on** button to keep previous trajectories on the plot for comparison.

6. **Reset:**  
   Click the **Reset** button to clear the plot and restore all settings to their default values.

## Code Structure
- **UI Components:**  
  The app utilizes MATLAB UI elements such as uifigure, uiaxes, numeric edit fields, and state/push buttons for interactive control.

- **Core Functionality:**  
  The `plotTrajectory` method handles the physics computations using projectile motion equations and plots the results. It calculates:
  - The time of flight using the quadratic equation.
  - The projectile's X and Y positions over time.
  - The maximum height and the horizontal distance at that point.
  - The landing (range) point.

- **Event Handling:**  
  Each button (for planetary selection, simulation, and reset) has an associated callback to manage UI state and trigger updates to the plot.

## Contributing
Contributions, suggestions, and bug reports are welcome. Feel free to fork the repository and submit pull requests with improvements or fixes.

## License
This project is released under the [MIT License](LICENSE).

## Acknowledgments
- Developed using MATLAB App Designer.
- Inspired by classical projectile motion physics and educational simulations.
