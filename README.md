# 6.2-Etch-a-Sketch

### Assignment: Build Your Own Etch-a-Sketch Program with Tkinter

In this assignment, you will create an interactive “Etch-a-Sketch” application using Tkinter. Your program will allow users to draw on a canvas using adjustable color settings and coordinate sliders. Follow the instructions below to complete this assignment.

---

#### Objective:
Create an interactive GUI where users can control the x and y coordinates of a line and adjust the color using sliders for red, green, and blue values. The user should be able to clear the canvas to start fresh.

### Requirements:

1. **Basic Setup**
   - Import Tkinter using `from tkinter import *`.
   - Initialize the main window with the title **"Etch-a-Sketch"**.
   - Set the main window size to `1000x800` and a background color of your choice.

2. **Define Variables**
   - Use `IntVar` to create variables for red, green, blue values (each ranging from 0-255).
   - Set initial values for red, green, and blue to make the color start as white (`255, 255, 255`).
   - Create `IntVar` variables for `x`, `y`, `oldx`, and `oldy` to track the current and previous coordinates.

3. **Functions**
   - **draw_line(event):**
     - Draw a line from `oldx`, `oldy` to `x`, `y` on a canvas.
     - Update `oldx` and `oldy` to the new `x`, `y` values after each line.
   
   - **change_color(event):**
     - Set `hex_color` by converting red, green, blue values to a hex string using `f"#{red.get():02x}{green.get():02x}{blue.get():02x}"`.
   
   - **clear_canvas():**
     - Clear all drawings from the canvas.

4. **Add Widgets**
   - **Sliders for RGB Values:**
     - Create three horizontal sliders (Scale widgets) to adjust the red, green, and blue color components.
     - Each slider should have a distinct background color (`red`, `green`, `blue`).
     - Set `command=change_color` so that adjusting any slider updates the color instantly.

   - **Sliders for X and Y Coordinates:**
     - Create horizontal and vertical sliders for controlling the x and y coordinates.
     - Set their `command=draw_line` so that moving a slider draws a line to the new coordinates.

   - **Clear Button:**
     - Add a button labeled "Clear" to clear the canvas.
     - Connect the button’s command to `clear_canvas`.

5. **Canvas**
   - Add a canvas widget where the drawing will take place. Set its background to black.

6. **Labels**
   - Place a label at the top of the window with the title **"Etch-a-Sketch"** in large font.

---

### Grading Rubric (100 Points):

1. **Setup and Initialization (10 points)**
   - Correct window title, size, and background color.

2. **Variables (10 points)**
   - Proper use of `IntVar` for red, green, blue, x, y, oldx, and oldy.

3. **Functions (30 points)**
   - `draw_line()` function works correctly (15 points).
   - `change_color()` function properly updates color (10 points).
   - `clear_canvas()` function clears the canvas (5 points).

4. **Sliders and Button (30 points)**
   - RGB sliders correctly adjust color (10 points).
   - Coordinate sliders correctly draw lines (10 points).
   - Clear button functions as expected (10 points).

5. **Canvas and Labels (10 points)**
   - Canvas is in the correct location, has a black background, and displays lines as expected.
   - Title label is visible and well-placed.

6. **Creativity and Usability (10 points)**
   - Program is visually appealing and user-friendly.
   - Optional: Add a frame around the canvas or further customize the color options.

