# mplruler

This is an auxiliary library for displaying rulers and grids in matplotlib's Figure.

Although they do not remain on the final figure, auxiliary lines and scales make it easy to grasp the position and size of the figure and make adjustments smoothly.

`mlpruler` has two functions.

* `add_ruler`
  * Display ruler in inches

![ruler](./images/ruler.png)

* `add_grid`
  * Displays grid lines in fraction

![grid](./images/grid.png)


## Example

With grid lines, it is easy to keep track of the width and position of the axes.

![both](./images/both.png)


## Installation

```
pip install mplruler
```

## Usage

```python
from mplruler import add_ruler, add_grid

# make figure and plot something
fig, ax = plt.subplots()
ax.plot([1, 2, 4, 9])
ax.plot([0, 1, 2, 3])

# call one or both functions.
add_ruler(fig)
add_grid(fig)
```

## API

### add_ruler

```
fig : matplotlib.figure.Figure
    draw ruler on the figure
disable : bool (default: False)
    do nothing if true
increments: float (default: 0.1 inches)
    increments of ruler in inches
bar_height: float (default: 0.1 inches)
    bar height in inches
color: (default: "gray")
    color
lw: float (default: 1.0)
    line weight
zorder: float (default: 9.0)
    zorder of ruler
```

### add_grid

```
fig : matplotlib.figure.Figure
    draw grid on the figure
disable : bool (default: False)
    do nothing if true
num_grid: int (default: 10)
color: (default: "gray")
    color
lw: float (default: 1.0)
    line weight
ls: (default: dotted)
    line style
zorder: float (default: 9.0)
    zorder of grid
```
