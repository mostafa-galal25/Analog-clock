# Real-Time Analog-clock🕰️

Real-Time Analog Clock (OpenCV & NumPy)A live, graphical analog clock application built entirely using OpenCV and NumPy.
This project demonstrates real-time drawing and geometric calculations to accurately reflect the current system time.

# FeaturesReal-Time Animation🌟:

The clock hands update smoothly, including sub-second accuracy for the second hand.
Geometric Drawing:
Uses trigonometric functions (math.sin, math.cos) to calculate the exact endpoint coordinates for the hour, minute, and second hands.
Digital Display:
Shows the current Date (YYYY-MM-DD) and Digital Time (HH:MM:SS) in the corner for reference.
Customizable Hands:
Each hand is rendered with a distinct color and thickness:
Second Hand:Blue 
(Thin)Minute Hand:Cyan/Yellow 
(Medium)Hour Hand:Light Blue/Pink 
(Thick)Hour Markers: Numbers 1 through 12 are drawn on the clock face.

# Technologies UsedTechnologyPurposePythonCore programming language🛠️.

OpenCV (cv2)Used for creating the display window, drawing shapes (circles, lines), and displaying text in real-time.
NumPyUsed to initialize and manage the canvas (image array) efficiently.
mathEssential for calculating angular positions of the hands using trigonometry.
datetimeUsed to fetch the current system time (hour, minute, second, microsecond).

# Prerequisites📦

Ensure you have Python installed, and then install the necessary libraries:
pip install opencv-python numpy

Ensure Dependencies are Met:
Verify you have opencv-python and numpy installed (see Prerequisites).

# How to Run▶️

Execute the Python script from your terminal:
python your_clock_script_name.py
(Replace your_clock_script_name.py with the actual name of your Python file.) 
A window titled "clock" will open, displaying the analog clock synchronized with your system time.
To Exit: Press the 'q' key on your keyboard.

# Code Logic Highlights📐

The core functionality of the clock relies on converting time values into angular measurements:
Total Angle ($2\pi$ Radians = 360 Degrees):
The code converts time units into radians, starting from a baseline position (usually the 12 position).
Second Hand Calculation:
It uses a factor of $6$ (since $60 \text{ seconds} \times 6 \text{ degrees/second} = 360 \text{ degrees}$).
It includes the microsecond component for smooth, continuous movement.
Formula used for angle (in radians):
$\text{sec} = \text{radians}((\text{current\_second} + \text{microseconds}) \times 6 - 90)$Hand Coordinates: The position of each hand's tip is calculated using the center $(C_x, C_y)$, the hand's length (radius $R$), and the calculated angle ($\theta$):$$X = C_x + R \cdot \cos(\theta) \\
Y = C_y + R \cdot \sin(\theta)


# Contributing🤝

Feedback and contributions are welcome!
Feel free to fork the repository and submit pull requests for improvements such as:Adding tick marks for minutes and seconds.
Implementing a digital/analog switch.
Improving performance or cleanup.


# License📄

Distributed under the MIT License. See LICENSE for more information.
