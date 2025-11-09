<!-- command: render -->

# Project 1 – Blink and Branch

**Course:** Engineering: Electronics and Computer Programming  
**Project Length:** 1 week  
**Objective:** Learn to write and upload MicroPython code to the Raspberry Pi Pico W, control an LED, and document your work using Git and GitHub.

---

## Overview

This is your first hands-on project with the Raspberry Pi Pico W.  
You will connect an LED to your board, write MicroPython code to make it blink, and modify that code so the pattern changes based on a condition in your program.  
You will also commit your work to GitHub and write a short reflection.

This project introduces three key ideas:
1. How code controls hardware.
2. How logical conditions and loops work in Python.
3. How to use Git and GitHub to track and share your progress.

---

## Learning Goals

By the end of this project, you should be able to:

- Use **Thonny** to edit and run code on your Pico W.
- Write and modify simple MicroPython programs using loops and conditionals.
- Wire a basic LED circuit using a breadboard and resistor.
- Commit your code to a GitHub repository with clear messages.
- Describe how software and hardware interact.

---

## Materials

- Raspberry Pi Pico W  
- Breadboard  
- 1 LED  
- 1 resistor (220–330 Ω)  
- 3 jumper wires (male-to-male)  
- USB cable for Pico W  
- Computer with Thonny and GitHub account
- Possilby other components for greater challenge.  

---

## Circuit Setup

1. Insert the Pico W into the breadboard.  
2. Connect using jumper wires:
   - **GP15** → one end of the resistor → **anode** (long leg) of LED.  
   - **GND** → **cathode** (short leg) of LED.  
3. Double-check polarity — the LED only works one way.

---

## Step 1 – Blink the LED

Download the starter repo from GitHub Classroom. There will be this code in the file names `blink.py`. 
```python
from machine import Pin, sleep
import time

led = Pin(15, Pin.OUT)

while True:
    led.value(1)
    time.sleep(0.5)
    led.value(0)
    time.sleep(0.5)
```

Run the code. Your LED should blink on and off every half second.

---

## Step 2 – Branch the Behavior

Modify your program to create a **branch** — a choice in behavior based on a variable.

For example, you could:

- Change the blink speed based on a variable called `mode`. 
- Let mode be randomly determined.
- Add a condition that blinks **twice fast** if `mode == 1` and **once slowly** if `mode == 2`.



---

## Step 3 – Document Your Work in GitHub

1. Add a file to your repository named `reflection.md` where you will discuss what you did and why you made the choices that you did. If something didn't work document it here, and describe what you tried to ovecome the issue. If everything worked, see how far you can push the idea. Don't quit till something is a challenge. 

2. Commit and push your work to GitHub with a clear message:
   ```
   git add .
   git commit -m "Initial version of Blink and Branch project"
   git push
   ```

---

## Step 4 – Reflection

Create a short Markdown file called `reflection.md` with 3–5 sentences answering:

1. What did your code do?  
2. How did you change the behavior using logic or variables?  
3. What challenges did you run into setting up the circuit or code?  
4. How did committing your code to GitHub help track your progress?

---

## Ideas for Extensions (Optional)

If you finish early:
- Add a **second LED** with a different pin and alternate them.
- Add a **button** that switches between blink modes.
- Control blink speed with a **potentiometer** as an analog input.

---

## Deliverables

| File | Description |
|------|--------------|
| `blink.py` | Working MicroPython code controlling LED blink pattern |
| `reflection.md` | Short reflection answering the four questions |
| `README.md` | This project description |
| GitHub repo | Contains code, documentation, and commit history |

**Due:** At the start of class next week.  
Your instructor will verify functionality and review your commits.

---

## Evaluation Criteria

| Category | Points | Description |
|-----------|--------|-------------|
| Functionality | 25 | LED blinks correctly and logic branch changes behavior |
| Code Quality | 25 | Code is readable, uses good structure and comments |
| Documentation | 20 | Reflection and README are clear and complete |
| GitHub Usage | 20 | Commits show progress; files organized in repo; good commit messages |
| Challenge | 10 | It is clear that the student found something challenging from their reflection |


**Total: 100 points**

---

### Notes
- Make sure your Thonny interpreter is set to **MicroPython (Raspberry Pi Pico)**.
- If your Pico doesn’t appear, unplug and reconnect while holding **BOOTSEL**, then reselect the interpreter.
- Always test your circuit before committing code.

---
