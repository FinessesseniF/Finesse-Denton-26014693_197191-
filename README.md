# creative-coding-template
SELECTION #1
p5.js - Week #6 Exercise #3
'Digital Loom'
My best P5 entry, this uses the technique of drawing the background in the canvas, rather than the draw space. Using a single tracking square (the 'Shuttle'), it 'paints' cells according to one of several noise variables and a LOT of if;else statements. I'm not sure this is the most efficient way to perform something like this, but it worked :).

To break it down:
the Shuttle is a square that moves (translates) right > down, left (on hitting border) > down,right (on hitting other border) and so on. It changes its colour based on how many 'steps' have been completed since hitting a wall. Its translation is tracked using a 'Shape X' (ShX) variable, which also determines the colour input of the shape based on the relative position (see: number) of the ShX variable. It selects from a list of noise variables that are then plugged into colour selectors (see: the mess of if;else statements), and then leaves that cell highlighted that colour.
For the pattern, I used the quirkiness of the ShX tracking (for some reason it kept offsetting its amount whenever it hit a border, so I just worked that into the pattern) to create three 'zipper' kind of shapes, surrounded by (usually) red cells. Each cell is a pre-set colour, the tone of which is slightly modified by the noise variables. Super happy with the outcome!
The 

SELECTION #2
p5.js - Week #4 Exercise #2
'Carpet'
This is another nice image, no animation whatsoever but I love the look of it. It reminds me of Islamic geometric patterns/motifs, which is what I was inspired by for this.
Mainly composed of the background pattern (nested for-loop creating overlapping ellipses), and the star+lozenges in the foreground (a complex mess of beziers).

To break it down:
Background - Again, a nested for-loop cretaing an overlapping field of ellipses, slightly offset to square it on the canvas.
The Star Shape - using beginshape(), I combined 4 bezier vertices originating at the topmost point of the star and going around counter(I believe?)clockwise. This was a bittcchhh to get right.
The Lozenges - these were far simpler, also using beginshape() and beziers, it was difficult to get the exact coordinates of the control points for each shape, BUT, the carpet background actually breaks the canvas up quite neatly into eigths, which was super helpful in locating said coordinates.
And that's basically it! super simple.

SELECTION #3
p5.js - Week #3 Exercise #2
'Night Climb'
Look I'll be honest, I wanted to put in my Wk6 Ex1 as this entry, but I accidentally overwrote the code for it in Week 7 :// Big regret.
I like this piece because it was difficult to get to work properly! the idea was to have a ladder scrolling infinitely down the screen, with shooting stars flying down in the background behind it.
In reality, it looks pretty shabby, but it works.

To break it down:
The Ladder - The ladder is a series of rectangles all using the same variable to scroll down the screen (offset vertically to give the appearance of being the same rungs scrolling down), which resets when the middlemost rung (the one using dropY as raw input) hits a point offscreen, resetting the group.
The Star - The star is comprised of two elipses - one circular and one lozenge - and uses a separate variable for downward movement, and a random dropX variable for its 'spawn'(see: reset)point. This... does not work that well. Sometimes it disappears (I think it's behind the left leg of the ladder??) and falls in the same place twice in a row FREQUENTLY.
Again, Would that I were able, a different piece would have gone here. Oh well.
SELECTION #4
Touchdesigner - Week # Exercise #
SELECTION #5
Touchdesigner - Week # Exercise #
SELECTION #6
Touchdesigner - Week # Exercise #
