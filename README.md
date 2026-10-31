**Hello, this is PlantPal**

PlantPal is a beginner-friendly hydration tracker created in Python Mode for Processing. It encourages users to drink water by turning their daily hydration goal into a small virtual garden.

Each time the user records a cup of water, their selected plant grows. After eight cups, the user's garden adds the completed flower.

Why I created PlantPal:
I often forget to drink water, and my partner regularly reminds me to drink so I do not become dehydrated or get headaches. I wanted to create something that made hydration feel more rewarding and enjoyable.

PlantPal was inspired by the reward system used in the Forest focus app. However, PlantPal applies the idea to hydration: instead of growing a tree by staying focused, users grow flowers by drinking water.

**Features**
  - Eight-cup daily hydration goal
  - Plant growth after each cup
  - Three plant options: daisy, sunflower and tulip
  - Virtual garden for completed plants
  - Daily streak counter
  - 30-minute hydration timer
  - Today and Garden screens
  - Progress automatically saved to a text file
  - No external images or Python libraries required

**Built with**
  - Processing
  -  Processing Python Mode
  - Basic Python concepts such as variables, lists, loops, functions and conditional statements
  - Processing drawing functions such as ellipse(), rect(), line() and beginShape()

**How to run the project**
  1. Download and install Processing.
  2. Install or select Python Mode in Processing.
  3. Download the PlantPal_Processing_Python project folder.
  4. Open PlantPal_Processing_Python.pyde in Processing.
  5. Check that Python Mode is selected.
  6. Press the Run button.

**How to use PlantPal**
  1. Use the left and right arrows to select a flower.
  2. Press I drank a cup whenever you drink water.
  3. Watch the plant grow across eight stages.
  4. Complete eight cups to add the flower to your garden.
  5. Select Garden at the bottom to view collected plants.
  6. Use Start, Pause and Reset to control the hydration timer.

**Coding Examples**

Variables
Variables store information that can change:
cups = 0
streak = 0
selected_plant = 0

Conditional statements
The app uses conditions to decide when leaves and flowers should appear:
if stage >= 2:
    draw_leaf()

if stage >= DAILY_GOAL:
    draw_flower()

Loops
A loop creates the eight water-drop markers:
for index in range(DAILY_GOAL):
    draw_drop()

Functions
The project is divided into functions so each section has a clear purpose:
def log_cup():
    global cups
    cups += 1
    
**Saving progress**
PlantPal creates a file called plantpal_progress.txt inside the sketch's data folder. 
This file stores:
  - Number of cups
  - Current streak
  - Selected flower
  - Last completed date
  - Plants saved in the garden

**Challenges and learning**

One of the main challenges was understanding the difference between a regular Python application and Python Mode in Processing. Processing creates the interface using coordinates and drawing functions rather than regular application widgets.

I also needed to adjust the size and position of the flowers because the fully grown tulip originally overlapped with its name. Testing the interface helped me identify and correct this problem.

**Current limitations**
  - The reminder changes the window title rather than sending a phone notification.
  - The streak system is simplified for the prototype.
  - Only the 12 most recent plants are displayed.
  - The project is designed for desktop Processing rather than mobile devices.

**Future improvements**
  - More unlockable flowers and pots
  - Custom daily water goals
  - Sound effects and animations
  - A hydration history calendar
  - More detailed streak tracking
  - Desktop or mobile notifications
  - User-selected reminder times

**Acknowledgements**
  - Forest provided inspiration for the visual reward and virtual garden concept.
  - LinkedIn Learning's Python for Students supported my early Python learning.
  - Processing documentation and tutorials supported the development of the interface and drawings.
