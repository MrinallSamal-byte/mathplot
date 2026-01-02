# Welcome to Matplotlib Master! 🎨📊

Hello! I'm **Matplotlib Master**, your patient and thorough Python programming tutor specializing in Matplotlib—the most powerful and widely-used data visualization library in Python.

## About Me

I'm here to guide you through every aspect of Matplotlib, from creating your very first plot to crafting publication-quality figures with advanced customizations. My teaching style is:

- **Patient**: We'll take things step by step, never rushing through concepts
- **Encouraging**: Every question is a good question, and mistakes are learning opportunities
- **Clear**: I explain concepts in simple language first, then add technical details
- **Thorough**: We'll cover ALL of Matplotlib's capabilities

## Before We Begin

Let me learn a bit about you! This helps me tailor the lessons to your needs:

**Assessment Questions:**
1. How comfortable are you with Python programming?
   - Beginner (just started learning Python)
   - Intermediate (familiar with functions, lists, dictionaries)
   - Advanced (comfortable with classes, modules, etc.)

2. Have you created plots or charts before?
   - Never created any plots
   - Used spreadsheet tools (Excel, Google Sheets)
   - Used other plotting libraries (Seaborn, Plotly, etc.)
   - Used Matplotlib a little bit

3. What's your main goal?
   - Learn data visualization for school/university
   - Create plots for research or publications
   - Build dashboards or reports
   - Just exploring and learning for fun

---

## Your Learning Journey: The Curriculum

Here's the structured path we'll follow (we'll progress at YOUR pace):

### 📚 Module 1: Installation and Your First Plot
- Setting up Matplotlib
- Understanding what Matplotlib does
- Creating your very first plot
- The magic of `plt.show()`

### 📚 Module 2: Pyplot Basics
- The pyplot interface (`plt`)
- Line plots in detail
- Customizing colors, labels, and titles
- The coordinate system

### 📚 Module 3: Object-Oriented Interface
- Understanding Figure and Axes
- Why use the OO approach?
- Creating plots the "proper" way
- When to use pyplot vs. OO

### 📚 Module 4: Plot Types and Customization
- Scatter plots
- Bar charts and histograms
- Pie charts
- Markers, linestyles, and colors
- Legends and grids
- Multiple lines on one plot

### 📚 Module 5: Layouts and Subplots
- Creating subplots
- Sharing axes
- Complex layouts with GridSpec
- Figure size and aspect ratios

### 📚 Module 6: Advanced Customization
- Text and annotations
- Arrows and shapes
- Mathematical expressions (LaTeX)
- Colormaps and colorbars
- Contour plots and heatmaps

### 📚 Module 7: 3D and Specialized Plots
- 3D plotting basics
- Surface plots and wireframes
- Polar plots
- Box plots and violin plots

### 📚 Module 8: Styles, Themes, and Publication Quality
- Using built-in styles
- Seaborn integration
- Custom rcParams
- DPI, formats, and saving figures
- Transparent backgrounds

### 📚 Module 9: Animation and Interactivity
- Creating animations
- Interactive plots
- Event handling
- Widgets and sliders

### 📚 Module 10: Integration and Best Practices
- Working with Pandas DataFrames
- NumPy arrays and Matplotlib
- Performance optimization
- Common pitfalls and how to avoid them
- Professional workflows

---

## How This Tutorial Works

For each concept we explore, I'll:

1. **Explain what it is and why it matters**
2. **Show you a minimal working example** (copy-paste ready!)
3. **Walk through the code line by line**
4. **Provide a more complex variation**
5. **Give you an exercise to try**
6. **Wait for your response or questions**

You can:
- Ask questions at ANY time
- Request clarification on anything
- Share your code for debugging help
- Skip ahead if you already know something
- Go back to review earlier concepts

---

## Let's Start! Module 1: Installation and Your First Plot

### What is Matplotlib?

Think of Matplotlib as your digital canvas and paintbrush for data. Just as an artist uses brushes to paint pictures, you use Matplotlib to paint with data—turning numbers into visual stories that people can understand at a glance.

**Why does it matter?**
- Numbers alone can be overwhelming
- Visual patterns are easier to spot than tables of data
- Good visualizations communicate insights effectively
- It's an essential skill for data science, research, and analysis

### Installing Matplotlib

If you haven't installed Matplotlib yet, it's super easy:

```python
# Using pip (most common)
pip install matplotlib

# Using conda (if you use Anaconda)
conda install matplotlib
```

**How to check if it's installed:**

```python
import matplotlib
print(matplotlib.__version__)
```

This should print the version number (like `3.8.0` or similar). If you get an error, the installation didn't work.

### Your Very First Plot! 🎉

Let's create something immediately. Here's the simplest possible plot:

```python
import matplotlib.pyplot as plt

# Create some data
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

# Create the plot
plt.plot(x, y)

# Display the plot
plt.show()
```

**Let me explain line by line:**

1. `import matplotlib.pyplot as plt` - We import the pyplot module and nickname it `plt` (shorter to type!)
2. `x = [1, 2, 3, 4, 5]` - Our x-axis values (horizontal)
3. `y = [2, 4, 6, 8, 10]` - Our y-axis values (vertical)
4. `plt.plot(x, y)` - This creates a line plot connecting the points
5. `plt.show()` - This actually displays the plot window

**Try running this code!** You should see a window with a blue line going from bottom-left to top-right.

### Making It Better

Let's add some labels so people know what they're looking at:

```python
import matplotlib.pyplot as plt

# Data
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

# Create the plot
plt.plot(x, y)

# Add labels and title
plt.xlabel('Input Values')
plt.ylabel('Output Values')
plt.title('My First Matplotlib Plot')

# Display
plt.show()
```

**What's new:**
- `plt.xlabel()` - Labels the horizontal axis
- `plt.ylabel()` - Labels the vertical axis
- `plt.title()` - Gives your plot a title

### A Slightly More Complex Example

Let's plot something more interesting—a sine wave!

```python
import matplotlib.pyplot as plt
import numpy as np

# Create x values from 0 to 10, with 100 points
x = np.linspace(0, 10, 100)

# Calculate y as sine of x
y = np.sin(x)

# Create the plot with some style
plt.plot(x, y, color='red', linewidth=2, label='sin(x)')

# Customize
plt.xlabel('x values')
plt.ylabel('sin(x)')
plt.title('Sine Wave Visualization')
plt.legend()  # Shows the label
plt.grid(True)  # Adds a grid

# Display
plt.show()
```

**What's new here:**
- `np.linspace(0, 10, 100)` - Creates 100 evenly spaced points from 0 to 10
- `color='red'` - Makes the line red
- `linewidth=2` - Makes the line thicker
- `label='sin(x)'` - Names the line (shown in legend)
- `plt.legend()` - Displays a legend box
- `plt.grid(True)` - Adds a helpful grid

### 🎯 Your First Exercise

Try modifying the sine wave example:

1. Change the color to 'green'
2. Change the title to something fun
3. Add a second line plotting `np.cos(x)` with label 'cos(x)'
4. Make the cosine line blue and dashed (hint: use `linestyle='--'`)

**Example solution pattern:**
```python
# After the first plot:
y2 = np.cos(x)
plt.plot(x, y2, color='blue', linewidth=2, linestyle='--', label='cos(x)')
```

**Ready to move on? What would you like to explore next?**

---

## Module 2: Pyplot Basics

Now that you've created your first plots, let's understand pyplot more deeply.

### What is Pyplot?

Pyplot is the **state-based interface** to Matplotlib. Think of it like giving commands to a painter:
- "Draw a line here"
- "Add a title"
- "Change the color"

Each `plt` command works on the "current" figure and axes. It's like pyplot remembers where you're working.

### The Coordinate System

Understanding coordinates is crucial:

```python
import matplotlib.pyplot as plt

# When you plot (x, y) pairs
plt.plot([0, 1, 2], [0, 1, 4])
#        x values   y values

plt.show()
```

- The first point is at (0, 0) - origin
- Second point is at (1, 1) - middle
- Third point is at (2, 4) - upper right

### Line Plots in Detail

Let's explore all the ways to customize lines:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 10, 50)

# Different line styles
plt.plot(x, np.sin(x), linestyle='-', label='solid')
plt.plot(x, np.sin(x) + 0.5, linestyle='--', label='dashed')
plt.plot(x, np.sin(x) + 1.0, linestyle='-.', label='dash-dot')
plt.plot(x, np.sin(x) + 1.5, linestyle=':', label='dotted')

plt.legend()
plt.title('Different Line Styles')
plt.show()
```

**Common linestyles:**
- `'-'` or `'solid'` - solid line (default)
- `'--'` or `'dashed'` - dashed line
- `'-.'` or `'dashdot'` - dash-dot line
- `':'` or `'dotted'` - dotted line

### Colors: Many Ways to Specify

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 10, 100)

# Method 1: Named colors
plt.plot(x, np.sin(x), color='red', label='red')

# Method 2: Short codes
plt.plot(x, np.sin(x) + 1, color='b', label='blue')  # 'b' for blue

# Method 3: Hex codes
plt.plot(x, np.sin(x) + 2, color='#FF5733', label='hex')

# Method 4: RGB tuples (values 0-1)
plt.plot(x, np.sin(x) + 3, color=(0.1, 0.8, 0.3), label='RGB')

plt.title('Different Ways to Specify Colors')
plt.legend()
plt.show()
```

**Common color codes:**
- `'b'` - blue
- `'g'` - green
- `'r'` - red
- `'c'` - cyan
- `'m'` - magenta
- `'y'` - yellow
- `'k'` - black
- `'w'` - white

### Markers: Adding Points

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [1, 4, 9, 16, 25]

plt.plot(x, y, 
         marker='o',           # Circle markers
         markersize=10,        # Size of markers
         markerfacecolor='red', # Fill color
         markeredgecolor='black', # Edge color
         markeredgewidth=2)    # Edge thickness

plt.title('Plot with Markers')
plt.show()
```

**Common markers:**
- `'o'` - circle
- `'s'` - square
- `'^'` - triangle up
- `'v'` - triangle down
- `'*'` - star
- `'+'` - plus
- `'x'` - x mark
- `'D'` - diamond

### Combining Style Elements

You can use a shorthand format string:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [1, 4, 9, 16, 25]

# Format string: [marker][line][color]
plt.plot(x, y, 'ro-')  # red circles with solid line
# Same as: marker='o', linestyle='-', color='r'

plt.title('Shorthand Format')
plt.show()
```

**Format string examples:**
- `'b-'` - blue solid line
- `'ro'` - red circles (no line)
- `'g^:'` - green triangles with dotted line
- `'k--'` - black dashed line

### 🎯 Exercise: Create a Multi-line Plot

Create a plot showing three mathematical functions:
1. y = x² (red, solid line, circle markers)
2. y = x³ (blue, dashed line, square markers)
3. y = 2ˣ (green, dotted line, triangle markers)

Use x values from 0 to 5.

**Have you tried the exercise? What challenges did you face?**

---

## Module 3: Object-Oriented Interface

This is where Matplotlib gets more powerful! Let's learn the "professional" way to create plots.

### Why Use Object-Oriented (OO) Approach?

The pyplot interface is great for quick plots, but it has limitations:
- Hard to work with multiple figures
- Difficult to customize complex layouts
- Less control over individual elements

The OO approach gives you:
- Explicit control over figures and axes
- Better for complex visualizations
- Easier to reuse and organize code
- Industry standard for serious work

### Understanding Figure and Axes

**Analogy time!** Think of Matplotlib plotting like painting:
- **Figure** = The canvas/paper you paint on
- **Axes** = The actual drawing area (can have multiple on one canvas)
- **Axis** = The x or y axis lines (don't confuse with Axes!)

```python
import matplotlib.pyplot as plt

# Create a figure and one axes
fig, ax = plt.subplots()

# Now we work with 'ax' instead of 'plt'
ax.plot([1, 2, 3], [1, 4, 9])
ax.set_xlabel('X Label')
ax.set_ylabel('Y Label')
ax.set_title('OO Interface Example')

plt.show()
```

**Key differences:**
- `plt.subplots()` creates and returns figure and axes objects
- Use `ax.plot()` instead of `plt.plot()`
- Use `ax.set_xlabel()` instead of `plt.xlabel()`
- Use `ax.set_title()` instead of `plt.title()`

### A Complete Example

```python
import matplotlib.pyplot as plt
import numpy as np

# Create figure and axes
fig, ax = plt.subplots(figsize=(10, 6))  # Size in inches

# Generate data
x = np.linspace(0, 10, 100)
y1 = np.sin(x)
y2 = np.cos(x)

# Plot on the axes
ax.plot(x, y1, 'b-', label='sin(x)', linewidth=2)
ax.plot(x, y2, 'r--', label='cos(x)', linewidth=2)

# Customize the axes
ax.set_xlabel('x values', fontsize=12)
ax.set_ylabel('y values', fontsize=12)
ax.set_title('Sine and Cosine Functions', fontsize=14, fontweight='bold')
ax.legend(loc='upper right')
ax.grid(True, alpha=0.3)  # Transparent grid

# Set axis limits
ax.set_xlim(0, 10)
ax.set_ylim(-1.5, 1.5)

plt.show()
```

**New concepts:**
- `figsize=(10, 6)` - Figure size in inches (width, height)
- `fontsize=12` - Control text size
- `fontweight='bold'` - Make text bold
- `loc='upper right'` - Legend position
- `alpha=0.3` - Transparency (0=invisible, 1=opaque)
- `ax.set_xlim()` and `ax.set_ylim()` - Control axis ranges

### Multiple Subplots

Here's where the OO approach really shines:

```python
import matplotlib.pyplot as plt
import numpy as np

# Create 2x2 grid of subplots
fig, axes = plt.subplots(2, 2, figsize=(10, 8))

# 'axes' is a 2D array of axes objects
x = np.linspace(0, 10, 100)

# Top-left: sine
axes[0, 0].plot(x, np.sin(x), 'b-')
axes[0, 0].set_title('Sine')
axes[0, 0].grid(True)

# Top-right: cosine
axes[0, 1].plot(x, np.cos(x), 'r-')
axes[0, 1].set_title('Cosine')
axes[0, 1].grid(True)

# Bottom-left: tangent
axes[1, 0].plot(x, np.tan(x), 'g-')
axes[1, 0].set_title('Tangent')
axes[1, 0].set_ylim(-5, 5)  # Limit y-axis
axes[1, 0].grid(True)

# Bottom-right: exponential
axes[1, 1].plot(x, np.exp(x/5), 'm-')
axes[1, 1].set_title('Exponential')
axes[1, 1].grid(True)

# Add overall title
fig.suptitle('Trigonometric and Exponential Functions', fontsize=16)

# Adjust spacing
plt.tight_layout()

plt.show()
```

**Important concepts:**
- `plt.subplots(2, 2)` - Creates 2 rows, 2 columns
- `axes[row, col]` - Access individual subplot
- `fig.suptitle()` - Overall figure title
- `plt.tight_layout()` - Auto-adjust spacing (prevents overlap)

### When to Use What?

**Use pyplot (`plt.plot()`) when:**
- Making quick exploratory plots
- Simple, single plots
- Interactive sessions (Jupyter notebooks)

**Use OO interface (`fig, ax`) when:**
- Multiple subplots
- Complex customization
- Writing reusable functions
- Professional/publication work
- Need precise control

**Does the OO interface make sense to you? Any questions?**

---

## Module 4: Plot Types and Customization

Let's explore the different types of visualizations you can create!

### Scatter Plots

Perfect for showing relationships between two variables:

```python
import matplotlib.pyplot as plt
import numpy as np

# Generate random data
np.random.seed(42)
x = np.random.randn(100)
y = 2 * x + np.random.randn(100) * 0.5

# Create scatter plot
fig, ax = plt.subplots(figsize=(8, 6))

ax.scatter(x, y, 
           c='blue',        # Color
           s=50,           # Size
           alpha=0.6,      # Transparency
           edgecolors='black',  # Edge color
           linewidth=0.5)  # Edge width

ax.set_xlabel('X Variable')
ax.set_ylabel('Y Variable')
ax.set_title('Scatter Plot Example')
ax.grid(True, alpha=0.3)

plt.show()
```

**Color mapping by value:**

```python
import matplotlib.pyplot as plt
import numpy as np

np.random.seed(42)
x = np.random.randn(100)
y = np.random.randn(100)
colors = x + y  # Color based on sum

fig, ax = plt.subplots(figsize=(8, 6))

scatter = ax.scatter(x, y, c=colors, s=100, cmap='viridis', alpha=0.6)

# Add colorbar
plt.colorbar(scatter, ax=ax, label='Value')

ax.set_xlabel('X')
ax.set_ylabel('Y')
ax.set_title('Scatter Plot with Color Mapping')
ax.grid(True)

plt.show()
```

### Bar Charts

Great for comparing categories:

```python
import matplotlib.pyplot as plt

# Data
categories = ['A', 'B', 'C', 'D', 'E']
values = [23, 45, 56, 78, 32]

fig, ax = plt.subplots(figsize=(8, 6))

# Vertical bars
bars = ax.bar(categories, values, 
               color='skyblue',
               edgecolor='navy',
               linewidth=2)

# Customize individual bars
bars[2].set_color('red')  # Highlight third bar

ax.set_xlabel('Categories')
ax.set_ylabel('Values')
ax.set_title('Bar Chart Example')
ax.grid(True, axis='y', alpha=0.3)

plt.show()
```

**Horizontal bar chart:**

```python
import matplotlib.pyplot as plt

categories = ['Python', 'Java', 'C++', 'JavaScript', 'Go']
popularity = [85, 70, 65, 80, 60]

fig, ax = plt.subplots(figsize=(8, 6))

ax.barh(categories, popularity, color='coral', edgecolor='black')

ax.set_xlabel('Popularity Score')
ax.set_title('Programming Language Popularity')
ax.grid(True, axis='x', alpha=0.3)

plt.show()
```

**Grouped bar charts:**

```python
import matplotlib.pyplot as plt
import numpy as np

# Data
languages = ['Python', 'Java', 'JavaScript']
year_2022 = [85, 70, 80]
year_2023 = [90, 72, 85]

x = np.arange(len(languages))
width = 0.35  # Width of bars

fig, ax = plt.subplots(figsize=(10, 6))

bars1 = ax.bar(x - width/2, year_2022, width, label='2022', color='skyblue')
bars2 = ax.bar(x + width/2, year_2023, width, label='2023', color='orange')

ax.set_xlabel('Programming Language')
ax.set_ylabel('Popularity Score')
ax.set_title('Programming Language Popularity Comparison')
ax.set_xticks(x)
ax.set_xticklabels(languages)
ax.legend()
ax.grid(True, axis='y', alpha=0.3)

plt.show()
```

### Histograms

For showing distributions:

```python
import matplotlib.pyplot as plt
import numpy as np

# Generate random data (normal distribution)
np.random.seed(42)
data = np.random.randn(1000)

fig, ax = plt.subplots(figsize=(10, 6))

# Create histogram
n, bins, patches = ax.hist(data, 
                            bins=30,          # Number of bins
                            color='steelblue',
                            edgecolor='black',
                            alpha=0.7)

ax.set_xlabel('Value')
ax.set_ylabel('Frequency')
ax.set_title('Histogram Example')
ax.grid(True, axis='y', alpha=0.3)

plt.show()
```

### Pie Charts

For showing proportions:

```python
import matplotlib.pyplot as plt

# Data
labels = ['Python', 'JavaScript', 'Java', 'C++', 'Others']
sizes = [30, 25, 20, 15, 10]
colors = ['#ff9999', '#66b3ff', '#99ff99', '#ffcc99', '#ff99cc']
explode = (0.1, 0, 0, 0, 0)  # Explode first slice

fig, ax = plt.subplots(figsize=(8, 8))

ax.pie(sizes, 
       explode=explode,
       labels=labels, 
       colors=colors,
       autopct='%1.1f%%',      # Show percentages
       startangle=90,           # Start angle
       shadow=True)             # Add shadow

ax.set_title('Programming Language Usage')

plt.show()
```

### Box Plots

For showing statistical distributions:

```python
import matplotlib.pyplot as plt
import numpy as np

# Generate random data
np.random.seed(42)
data = [np.random.normal(0, std, 100) for std in range(1, 4)]

fig, ax = plt.subplots(figsize=(8, 6))

box = ax.boxplot(data, 
                 labels=['Group 1', 'Group 2', 'Group 3'],
                 patch_artist=True,  # Fill with color
                 notch=True,         # Notched box
                 vert=True)          # Vertical

# Customize colors
for patch in box['boxes']:
    patch.set_facecolor('lightblue')

ax.set_ylabel('Values')
ax.set_title('Box Plot Example')
ax.grid(True, axis='y', alpha=0.3)

plt.show()
```

**Which plot type do you want to explore more?**

---

## Module 5: Layouts and Subplots

Let's master complex layouts!

### GridSpec: Advanced Layouts

For complex, non-uniform layouts:

```python
import matplotlib.pyplot as plt
import matplotlib.gridspec as gridspec
import numpy as np

fig = plt.figure(figsize=(12, 8))

# Create a 3x3 grid
gs = gridspec.GridSpec(3, 3, figure=fig)

# Large plot spanning 2x2 (top-left)
ax1 = fig.add_subplot(gs[0:2, 0:2])
ax1.plot(np.random.randn(100).cumsum())
ax1.set_title('Large Plot')

# Top-right
ax2 = fig.add_subplot(gs[0, 2])
ax2.hist(np.random.randn(1000), bins=20)
ax2.set_title('Histogram')

# Middle-right
ax3 = fig.add_subplot(gs[1, 2])
ax3.scatter(np.random.rand(50), np.random.rand(50))
ax3.set_title('Scatter')

# Bottom row spanning all columns
ax4 = fig.add_subplot(gs[2, :])
ax4.plot(np.random.randn(100), 'r-')
ax4.set_title('Wide Plot')

plt.tight_layout()
plt.show()
```

---

## Module 6: Advanced Customization

Time to make your plots publication-ready!

### Text and Annotations

```python
import matplotlib.pyplot as plt
import numpy as np

fig, ax = plt.subplots(figsize=(10, 6))

x = np.linspace(0, 10, 100)
y = np.sin(x)

ax.plot(x, y, 'b-', linewidth=2)

# Add text at specific position
ax.text(5, 0.5, 'Peak Region', fontsize=12, 
        ha='center', va='bottom')

# Annotate with arrow
ax.annotate('Maximum', 
            xy=(np.pi/2, 1),          # Point to annotate
            xytext=(2, 0.5),          # Label position
            fontsize=12,
            arrowprops=dict(facecolor='red', shrink=0.05))

# Another annotation
ax.annotate('Zero crossing', 
            xy=(np.pi, 0),
            xytext=(4, -0.5),
            fontsize=12,
            arrowprops=dict(arrowstyle='->', 
                          connectionstyle='arc3,rad=0.3',
                          color='green',
                          lw=2))

ax.set_title('Text and Annotations')
ax.grid(True)

plt.show()
```

### Mathematical Expressions (LaTeX)

```python
import matplotlib.pyplot as plt
import numpy as np

fig, ax = plt.subplots(figsize=(10, 6))

x = np.linspace(0, 2*np.pi, 100)
y1 = np.sin(x)
y2 = np.cos(x)

ax.plot(x, y1, label=r'$\sin(x)$')
ax.plot(x, y2, label=r'$\cos(x)$')

# LaTeX in title
ax.set_title(r'Trigonometric Functions: $\sin(x)$ and $\cos(x)$', 
             fontsize=14)

# LaTeX in labels
ax.set_xlabel(r'$x$ (radians)', fontsize=12)
ax.set_ylabel(r'$f(x)$', fontsize=12)

# Complex equation
ax.text(3, 0.5, r'$e^{i\pi} + 1 = 0$', fontsize=16,
        bbox=dict(boxstyle='round', facecolor='wheat', alpha=0.5))

ax.legend()
ax.grid(True)

plt.show()
```

**LaTeX syntax basics:**
- Wrap in `r'$ ... $'` for inline math
- `^` for superscript: `$x^2$`
- `_` for subscript: `$x_i$`
- `\frac{a}{b}` for fractions
- Greek letters: `\alpha`, `\beta`, `\gamma`, etc.

---

## Module 7: 3D and Specialized Plots

### 3D Plotting Basics

```python
import matplotlib.pyplot as plt
import numpy as np
from mpl_toolkits.mplot3d import Axes3D

fig = plt.figure(figsize=(12, 5))

# 3D line plot
ax1 = fig.add_subplot(131, projection='3d')
t = np.linspace(0, 10, 1000)
x = np.sin(t)
y = np.cos(t)
z = t
ax1.plot(x, y, z, 'b-', linewidth=2)
ax1.set_title('3D Line Plot')
ax1.set_xlabel('X')
ax1.set_ylabel('Y')
ax1.set_zlabel('Z')

# 3D scatter plot
ax2 = fig.add_subplot(132, projection='3d')
x = np.random.randn(100)
y = np.random.randn(100)
z = x**2 + y**2
ax2.scatter(x, y, z, c=z, cmap='viridis', s=50)
ax2.set_title('3D Scatter Plot')

# 3D surface plot
ax3 = fig.add_subplot(133, projection='3d')
x = np.linspace(-5, 5, 50)
y = np.linspace(-5, 5, 50)
X, Y = np.meshgrid(x, y)
Z = np.sin(np.sqrt(X**2 + Y**2))
surf = ax3.plot_surface(X, Y, Z, cmap='coolwarm', alpha=0.8)
ax3.set_title('3D Surface Plot')

plt.tight_layout()
plt.show()
```

---

## Module 8: Styles, Themes, and Publication Quality

### Built-in Styles

```python
import matplotlib.pyplot as plt
import numpy as np

# See all available styles
print(plt.style.available)

# Use a style
plt.style.use('seaborn-v0_8-darkgrid')

x = np.linspace(0, 10, 100)

plt.figure(figsize=(10, 6))
plt.plot(x, np.sin(x), label='sin(x)')
plt.plot(x, np.cos(x), label='cos(x)')
plt.title('Plot with Seaborn Style')
plt.legend()
plt.show()

# Reset to default
plt.style.use('default')
```

### Saving Figures

```python
import matplotlib.pyplot as plt
import numpy as np

fig, ax = plt.subplots(figsize=(10, 6))

x = np.linspace(0, 10, 100)
ax.plot(x, np.sin(x))
ax.set_title('Plot to Save')

# Save as PNG (raster)
plt.savefig('myplot.png', 
            dpi=300,              # High resolution
            bbox_inches='tight',  # Remove extra whitespace
            facecolor='white')    # Background color

# Save as PDF (vector)
plt.savefig('myplot.pdf', 
            bbox_inches='tight')

# Save with transparent background
plt.savefig('myplot_transparent.png', 
            dpi=300,
            bbox_inches='tight',
            transparent=True)

plt.show()
```

**Format options:**
- `'png'` - Raster, good for web
- `'pdf'` - Vector, best for publications
- `'svg'` - Vector, web-friendly
- `'jpg'` - Raster, smaller files

---

## Module 9: Animation and Interactivity

### Basic Animation

```python
import matplotlib.pyplot as plt
import matplotlib.animation as animation
import numpy as np

fig, ax = plt.subplots()

x = np.linspace(0, 2*np.pi, 100)
line, = ax.plot(x, np.sin(x))

ax.set_xlim(0, 2*np.pi)
ax.set_ylim(-1.5, 1.5)
ax.set_title('Sine Wave Animation')

def animate(frame):
    line.set_ydata(np.sin(x + frame/10))
    return line,

ani = animation.FuncAnimation(fig, animate, 
                             frames=200, 
                             interval=50,
                             blit=True)

# To save: ani.save('sine_wave.gif', writer='pillow', fps=20)

plt.show()
```

---

## Module 10: Integration and Best Practices

### Working with Pandas

```python
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np

# Create sample DataFrame
df = pd.DataFrame({
    'date': pd.date_range('2023-01-01', periods=100),
    'value1': np.cumsum(np.random.randn(100)),
    'value2': np.cumsum(np.random.randn(100)),
    'category': np.random.choice(['A', 'B', 'C'], 100)
})

fig, axes = plt.subplots(2, 2, figsize=(14, 10))

# Time series plot
df.plot(x='date', y=['value1', 'value2'], ax=axes[0, 0])
axes[0, 0].set_title('Time Series')

# Histogram
df['value1'].hist(ax=axes[0, 1], bins=20)
axes[0, 1].set_title('Histogram')

# Scatter plot
df.plot.scatter(x='value1', y='value2', ax=axes[1, 0])
axes[1, 0].set_title('Scatter Plot')

# Box plot
df.boxplot(column='value1', by='category', ax=axes[1, 1])
axes[1, 1].set_title('Box Plot by Category')

plt.tight_layout()
plt.show()
```

### Best Practices

1. **Always use the OO interface for production code**
```python
# Good
fig, ax = plt.subplots()
ax.plot(x, y)

# Not recommended for complex work
plt.plot(x, y)
```

2. **Close figures to save memory**
```python
fig, ax = plt.subplots()
ax.plot(x, y)
plt.show()
plt.close(fig)  # Free memory
```

3. **Use meaningful labels and titles**
```python
ax.set_xlabel('Time (seconds)', fontsize=12)
ax.set_ylabel('Temperature (°C)', fontsize=12)
ax.set_title('Temperature vs Time', fontsize=14)
```

4. **Choose appropriate plot types**
- Line plots: trends over time
- Scatter: relationships between variables
- Bar: comparisons between categories
- Histogram: distributions
- Box plot: statistical summaries

5. **Use consistent colors and styles**

### Common Pitfalls to Avoid

1. **Not using `plt.show()`** in scripts
2. **Overlapping labels** (use `plt.tight_layout()`)
3. **Too many colors** (limit to 5-7 distinct colors)
4. **Missing legends** (always label your data)
5. **Poor resolution** (use `dpi=300` for saving)
6. **Not closing figures** (memory leaks in long scripts)

### Performance Tips

```python
# Use downsampling for large datasets
x_large = np.linspace(0, 100, 1000000)
y_large = np.sin(x_large)

# Instead of plotting 1M points, downsample:
step = 1000
ax.plot(x_large[::step], y_large[::step])  # Much faster!
```

---

## Congratulations! 🎉

You've completed the Matplotlib Master curriculum! You now know:

✅ Installation and basic plotting
✅ Pyplot and OO interfaces
✅ All major plot types
✅ Complex layouts and subplots
✅ Advanced customization
✅ 3D and specialized plots
✅ Styles and themes
✅ Animation basics
✅ Integration with Pandas
✅ Best practices

### What's Next?

- Practice with real datasets
- Explore the [Matplotlib Gallery](https://matplotlib.org/stable/gallery/)
- Read the [official documentation](https://matplotlib.org/)
- Contribute to open source projects
- Create your own visualization library

### Keep Learning!

Remember:
- **Experiment**: Try changing every parameter to see what happens
- **Read examples**: The gallery has hundreds of examples
- **Ask questions**: The community is helpful
- **Practice**: The more you plot, the better you get

### Need Help?

If you have questions or want to explore specific topics deeper:
1. Share your code with me
2. Describe what you're trying to achieve
3. Show me any error messages

I'm here to help you master Matplotlib! What would you like to explore next?

---

**Ready to start your journey? Let's begin with Module 1!** 🚀

What's your current experience level with Python and plotting?
