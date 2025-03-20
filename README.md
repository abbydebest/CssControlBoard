# CssControlBoard process

## Introduction

# 🤎 Week 1

## Assignment choice
For this assignment we had to choose one of the following options: 1 creating a control board website(or something that is controlled with buttons), 2 implementing a film timeline into a interactive website or 3 the interaction of a rubiks cube in a website. I choose the first as it spoke to me the most, because I can come up with many different concepts for this and because I hope it will help me better my CSS and interaction skills. For the concept of this assigment I came up with multiple idea's of controlling of manipulating things:

* Type manipulator
* Image manipulator
* Some sort of customiser
* Lamps
* Record player
* Walkmann
* Flipable calendar

First I was very excited with my type manipulator idea, but it seemed like a hard concept to actually realise. I then choose to develop my lamp idea, of the ability to control a cute lamp and its properties such as light colour, warmth, intensity and effect. 

## Moodboard

## CSS techniques

I expect to use the following CSS techniques for these reasons:
* Grid/flexbox for creating a proper lay-out
* `:has()` attribute to create 'if statements' with CSS and change website based in input
* Effects and overlays, masks and clip paths's
* Custom properties for cause and action

## Challenges
I think the biggest challenge lies in creating a visually realistic lamp with light effect in code. And adding perspective.

## Sketches

## Feedback

* Iets toevoegen, muis/gezicht
* Easter egg
* 

# 🕯️ Week 2

## Start code
I stated with some base HTML for my lay-out and build up with some standard CSS(remedy) I typically use.

![Start of my code with some base HTML and standard CSS(remedy)](./images/process/screenshot-week2-start-code.png)

## Start lamp
### Lamp top shape(8 values border radius)
For the lamp I wanted to use as little HTML as possible, therefore I used CSS with `::before` and `::after` to create multiple shapes within the same HTML element. I used the `border-radius` property with all its eight values to manipulate the border of the `div`, to create the correct lamp shape.

![Shape of lamp top with 8-value border radius](./images/process/screenshot-week2-lamp-top-shape(8-values-border-radius).png)

### Shadow top shape(background image + gradients as mask)
By using the `background-image:` property and `linear-gradient()` function to create a linear gradient that imitates a shadow on the lamp. In combination with `background-size`, `background-position`, `background-repeat: no-repeat;` and adding a second radial shadow background image on top I created the same rounding effect in the shadow as the lamp shape has.

I also added the top indent effect with two radial shadows stacked on top of each other.

![Shadow on the top shape with two linear gradients as background images creating a sort of mask + top ident effect with two radial shadows stacked on top of each other](./images/process/screenshot-week2-shadow-top-shape(background%20image+gradients%20as-mask).png)

### Lamp foot shape(8 values border radius)
Used `::before` to make the lamp foot with the same `border-radius` technique as with the top shape

== Used `::before` for the foot, this way it is already positioned behind the lamp neck/stand shape that is an `::after` element ==

![Shape of the lamp foot with 8-value border radius](./images/process/screenshot-week2-lamp-foot-shape(8-value-border-radius).png)

### Lamp neck/stand shape(background image + transparent gradient)
I first tried making the stand shape with a clip path and even making my own svg, but this was not a success.

I added the stand with the `::after` selector and gradient to create two shapes with cut-outs. Achieving the desired cut-out shapes was a bit difficult to discover, but eventually a lot simpler than I anticipated.

![Shape of the lamp stand/neck with background images and transparent gradients](./images/process/screenshot-week2-lamp-neck-stand%20shape(background-image+transparent%20gradient).png)

Add image of gradient explained/drawn

I sized the `::after` element to the size I wanted it to be. After which I added two background gradients with their own cut-out on opposite sides. I wanted to achieve an 'elongated eclipse' shaped cut out, but when I sized up the transparent area(cut out) I lost most of the width in the shape, resulting in a super small neck/foot with a too short(not long/elongated enough) cut out. At first, I thought the best way to fix this was to add a third gradient in between to add some 'extra' body/width to the whole of the shape. Eventually I managed to fix this without an extra gradient, but by simply doubling the background-size to 200% and by making the cut out smaller, lowering the transparent em to 1.5em.

## The end result after week 2
![Result after week 2](./images/process/screenshot-week2-start-lamp.png)

## Feedback
* stack
* added 1px to gradient for smooth/blurred effect

# 🪩 Week 3

## Realistic lamp & controls
During this week I tried to make the lamp even more realistic and create a more complete scene. 

### Glow
I started by adding a realistic light glow using a simple `drop-shadow` on the lamp `<div>`. This also automatically added a glow to the before and after elements and so other parts of the lamp. Not neccessairly my intention but this is something I hope to fix later. *See glow at end result week 3*

### Shadow foot
For the shadow foot I once again applied the same technique of using a background image with gradient to create the illusion of a shadow. This time one shadow coming from the top of the shape and a sharp one on the bottom to create the illusion on an edge on the foot.

![Result of shadow on foot shape](./images/process/screenshot-week3-shadow-foot-result.png)
![Code of shadow on foot shape](./images/process/screenshot-week3-shadow-foot-code.png)

### Shadow stand
To make it super realistic I needed to add a shadow to the neck/stand shape. Since I already made the shape out of gradients, adding a shadow gradient on top would overlap the transparent cut-outs. I tried to think of a way to create the same cut-outs on the shadow and thought I might be able to use the `mask-image` property. I wasn't sure how to use it in such a 'complex' way so I asked Claude AI how to get my desired result. 

This made me realise I used the property wrong, but that I could in fact easily use it to create a shadow, by using the shadow as a background-image and using the mask-image property to create the neck/stand shape. So by doing things the other way around.

#### The shadow result before using mask-mage
![Result of shadow on stand/neck shape before using mask-image](./images/process/screenshot-week3-result-neck-shadow-before.png)
![Code of shadow on stand/neck shape before using mask-image](./images/process/screenshot-week3-neck-shadow-before-code.png)

#### The shadow result after using mask-mage
![Result of shadow on stand/neck shape with mask-image](./images/process/screenshot-week3-result-neck-shadow-after.png)
![Code of shadow on stand/neck shape with mask-image](./images/process/screenshot-week3-neck-shadow-after-code.png)

By using the gradients inside a mask I was able to create the shape into a mask using black and white. Then using the shadow gradient going from the shadow colour to the lamp colour as a background image. This way the lamp neck/stand has the shadow colour/effect and the mask with neck/stand shape is used as mask.

### Dresser
I then added a dresser with css shapes and a `transform: skewY();` effect to create the illusion of perspective. By adding a `:before` and `:after` element placing the :after more down and to the left.

![Dresser result](./images/process/screenshot-week3-dresser-css-shapes-result.png)
![Dresser code](./images/process/screenshot-week3-dresser-css-shapes-code.png)

### Controls
Lastly I added some controls in preparation of making the lamp and scene interactive.

![Controls code html]()

## The end result after week 3
![Result after week 3](./images/process/screenshot-week3-end-result.png)

## Feedback
* Try using 3D isometric or perspective
* CSS nesting (two reasons to use nesting: keep components together, structure in reading)
* Container queries
* Typography title and optional animation

# 🥟 Week 4

## Scene, light, styled radio buttons and dresser perspective

### Light effect div
To create the effect of 'actual' light coming of the lamp I added an extra `<div>` styled, sized and positioned exactly the same as the mushroom lamp top. Except placing it behind the actual lamp top and making it slightly bigger and blurred with `filter: blur();`. This way it gives the illusion of light. This is also the element I intend to control with the slider by making it bigger as the slider progresses. 

To make the light effect even more realistic, I added a `::before` and `::after` element to create light coming out of the bottom of the lamp and a cast of behind the lamp.

![Light effect div](./images/process/screen-recording-week4-light-effect-div.mov)

### Styled radio buttons
Because I had never really worked with inputs before I also did not know the best way to style them. I used a source that I had also used for radio buttons during the subject browser tech. The source used `::before` and `::after` element on the radio button, which is a great way to make more and very specific styling states, but was way to complicated for what I wanted to achieve. 

Which in this case was the radio button sizing down when checked and getting a thin border plus a small inset border to give it a depth/3d effect. Which I achieved by simply styling the `:checked` state of the radio button. 

I mirrored the inset shadow position on the `:checked` state to create a small animation effect(from 2em to -2em).

## Change colour lamp on :checked & make the html attribute with a colour value the lamp colour

## Making the shadow colour adjust to the lamp colour, chrome colour, light intensity slider and light/dark mode with container style queries

### Chrome colour


## The final result

## If I had more time on hand
