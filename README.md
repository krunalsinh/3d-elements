# 3D Letters

## 3D Letters text to life with three-dimensional effects. Designed to enhance the visual appeal of applications and websites, this UI allows developers to incorporate dynamically styled, interactive 3D letters into their projects.

In this project some advance CSS properties and concepts are used like CSS variables, CSS nesting, CSS calc(), etc. To make changes in this projects you should knowledge about CSS variables.

## Features

- We can modify letter color, position, and pattern.
- We can apply CSS keyframe animations.
- We can make letter properties configurable by implementing various classes.
- We can make letter positions predictable by using the `--cell-size` variable. 

### Prerequisites
- To work on or modify this project, you should have knowledge of CSS (including CSS variables and functions) and SCSS (with nesting).
- If you want to modify or implement new features, you'll need to compile SCSS into CSS.

### Installation Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/krunalsinh/3d-letters.git


### How to use

- All 3D elements must be children of the `.frame` element.
- The frame size is defined by the `--frame-size` CSS variable.
- The `--cell-size` CSS variable is crucial in this project, as it is used for all 3D space-related calculations. All dimensions and positions (height, width, XYZ position) are based on this variable.
- Each 3D element has four types of CSS classes:
   - #### `block`
     This class defines common properties such as position, rotation angle, and background color.
   - #### `letter-{{x}}`
     This class handles the individual properties of a 3D element, including its base XYZ position, height, width, and the size and position of nested elements.
   - #### `block-{{x}}`
     This class is responsible for all XYZ position-related calculations for the element.
   - #### `bg-{{x}}`
     This class defines the background color of the element.
- Each 3D element has its own height, width, depth, and XYZ positions.
- Every 3D element contains nested elements, which are defined by the `ele-{{x}}` class.
- Each nested element has six 3D sides, defined by the `.top`, `.bottom`, `.left`, `.right`, `.front`, and `.back` CSS classes.
- A 3D element may contain a nested element called `inner-3-cell`, which is used to horizontally center all nested elements. This is specifically used for elements with a width of `--cell-size * 3`.
- Each nested element has four types of variables defined in the `ele-{{x}}` class:
   - #### `--p-top`: Defines the element's position from the top.
   - #### `--p-left`: Defines the element's position from the left.
   - #### `--v-size`: Defines the element's vertical size.
   - #### `--h-size`: Defines the element's horizontal size.