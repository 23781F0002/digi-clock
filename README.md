# digi-clock
python program with clock
# Let's create the files for the Digital Clock project as requested by the user.
from pathlib import Path

# Define the project structure and content
project_path = Path("/mnt/data/digital-clock")
project_path.mkdir(exist_ok=True)

# clock.py content
clock_py_content = """import tkinter as tk
from time import strftime

# Create main window
root = tk.Tk()
root.title("Digital Clock")
root.geometry("400x200")
root.resizable(False, False)
root.configure(bg="black")

# Clock display
label = tk.Label(root, font=("Helvetica", 48), bg="black", fg="cyan")
label.pack(anchor="center", expand=True)

def update_time():
    current_time = strftime("%H:%M:%S")
    label.config(text=current_time)
    label.after(1000, update_time)  # Update every second

update_time()
root.mainloop()
"""

# requirements.txt content
requirements_content = "tk\n"

# README.md content
readme_content = """# Digital Clock ⏰

A simple **Digital Clock** built with Python and Tkinter.

## Features
- Displays current time in HH:MM:SS format
- Updates every second
- Simple GUI

## Requirements
- Python 3.x
- Tkinter (comes pre-installed with Python)

## Run the Project
```bash
python clock.py
