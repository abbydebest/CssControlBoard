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

## Start lamp
I stated with some base HTML for my lay-out and build up with some standard CSS(remedy) I typically use.

For the lamp I wanted to use as little HTML as possible, therefore I used CSS with `::before` and `::after` to create multiple shapes within the same HTML element. I used the `border-radius` property with all its eight values to manipulate the border of the `div`, to create the correct lamp shape. 

By using the `background-image: linear-gradient();` property and function to create a linear gradient that imitates a shadow on the lamp. In combination with `background-size`, `background-position`, `background-repeat: no-repeat;` and adding a second radial shadow background image on top I created the same rounding effect in the shadow as the lamp shape has.

* Tried making stand shape with clip path and making my own svg, not a success
* Used `::before` to make the lamp foot with the same `border-radius` technique
* I added the stand with the `::after` selector and gradient to create two shapes with cut-outs. Achieving the desired cut-out shapes was a bit difficult to discover, but eventually a lot simpler than I anticipated.

I sized the ::after element to the size I wanted it to be. After which I added two background gradients with their own cut-out on opposite sides. I wanted to achieve an 'elongated eclipse' shaped cut out, but when I sized up the transparent area(cut out) I lost most of the width in the shape, resulting in a super small neck/foot with a too short(not long/elongated enough) cut out. At first, I thought the best way to fix this was to add a third gradient in between to add some 'extra' body/width. Eventually I managed to fix this without an extra gradient, but by simply doubling the background-size to 200% and by making the cut out smaller, lowering the transparent em to 1.5em.

<img href="./images/Screenshot 2025-03-07 at 11.32.58.png">
