# Turtle experiment with fun math

A Python project that generates various colorful, dynamic geometric patterns and natural forms using Turtle graphics and custom color palettes.
It is made for my amusement and i usually add to it on long train rides 😌✌💖
## Usage

just run the cells, there is one for every function with a very brief description for each, there are a lot of parameters that can be tuned

## Cute generation examples

* These are random rainbow flowers

<img src="https://github.com/dsabi17/lines-and-stuff-i-think/blob/main/output/dandelions.png" width="400px" align="center">

* Flower-ception

<img src="https://github.com/dsabi17/lines-and-stuff-i-think/blob/main/output/flower_power_1.png" width="400px" align="center">

* Fractal tree with added noise and no symmetry, complementary angle pair of 30 - 60

<img src="https://github.com/dsabi17/lines-and-stuff-i-think/blob/main/output/tree_noise_no_symmetry.png" width="400px" align="center">

* Same story but with cherry tree skin

<img src="https://github.com/dsabi17/lines-and-stuff-i-think/blob/main/output/CHERRY_tree_noise_no_symmetry.png" width="400px" align="center">

* crazy composition

<img src="https://github.com/dsabi17/lines-and-stuff-i-think/blob/main/output/composition.png" width="400px" align="center">

there's more in the output folder :D

## Explaination for neeerdz

* Color palettes:
  * one_color_palette:
    * just keeps one color, no changes
  * rainbow_palette:
    * bad rainbow transition that goes through all the RGB spectrum
    * it increases one value and decreases one at a time
    * looks bad and muddy, it was fast   
  * good_rainbow_palette:
    * makes a smoother transition between the rainbow colors
    * interpolates between 2 colors at a time
  * cherry_palette:
    * made for the tree fractal
    * has handpicked colors
    * chooses colors bases on the depth of reccursion
    * picks the color based on a weight

* Functions for drawing:
  * dandelion
    * draws a dandelion-like pattern
    * repeatedly rotates and draws lines from a central point
    * the number of steps determines the number of lines and the angle of rotation.
  * flower_power
    * draws a layered flower pattern
    * calculates petal semi circle based on the precision parameter
    * the pattern is recursively drawn with decreasing size 
  * tree
    * classic tree fractal 
    * uses recursive helper function draw_branch
    * has a depth for the recursion
    * can add noise to the angles for a more natural look
    * there is a complementary mode for the angles to create agle pairs of (angle, 90° - angle)
  * triunghiul_psihedelic
    * recursive spiraling slightly offset triangle
 
* all of them have a dedicated cell for testing and for changing parameters
* the canvas is saved to a postscript file and it is set to exit on click, so you have to click on the screen at the end
* the last cell converts all the postscript files to .png, doesn't delete them
