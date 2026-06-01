# creative-coding-template
SELECTION #1
p5.js - Week #6 Exercise #3

['Digital Loom']
My best P5 entry, this uses the technique of drawing the background in the canvas, rather than the draw space. Using a single tracking square (the 'Shuttle'), it 'paints' cells according to one of several noise variables and a LOT of if;else statements. I'm not sure this is the most efficient way to perform something like this, but it worked :).

To break it down:

[The Shuttle] - Square that moves (translates) right > down, left (on hitting border) > down,right (on hitting other border) and so on. It changes its colour based on how many 'steps' have been completed since hitting a wall. Its translation is tracked using a 'Shape X' (ShX) variable, which also determines the colour input of the shape based on the relative position (see: number) of the ShX variable. It selects from a list of noise variables that are then plugged into colour selectors (see: the mess of if;else statements), and then leaves that cell highlighted that colour.
[The Pattern] - I used the quirkiness of the ShX tracking (for some reason it kept offsetting its amount whenever it hit a border, so I just worked that into the pattern) to create three 'zipper' kind of shapes, surrounded by (usually) red cells. Each cell is a pre-set colour, the tone of which is slightly modified by the noise variables. Super happy with the outcome!


SELECTION #2
p5.js - Week #4 Exercise #2

['Carpet']
This is another nice image, no animation whatsoever but I love the look of it. It reminds me of Islamic geometric patterns/motifs, which is what I was inspired by for this.
Mainly composed of the background pattern (nested for-loop creating overlapping ellipses), and the star+lozenges in the foreground (a complex mess of beziers).

To break it down:

[Background] - Again, a nested for-loop cretaing an overlapping field of ellipses, slightly offset to square it on the canvas.

[The Star Shape] - using beginshape(), I combined 4 bezier vertices originating at the topmost point of the star and going around counter(I believe?)clockwise. This was a bittcchhh to get right.

[The Lozenges] - these were far simpler, also using beginshape() and beziers, it was difficult to get the exact coordinates of the control points for each shape, BUT, the carpet background actually breaks the canvas up quite neatly into eigths, which was super helpful in locating said coordinates.
And that's basically it! super simple.

SELECTION #3
p5.js - Week #3 Exercise #2

['Night Climb']
Look I'll be honest, I wanted to put in my Wk6 Ex1 as this entry, but I accidentally overwrote the code for it in Week 7 :// Big regret.
I like this piece because it was difficult to get to work properly! the idea was to have a ladder scrolling infinitely down the screen, with shooting stars flying down in the background behind it.
In reality, it looks pretty shabby, but it works.

To break it down:

[The Ladder] - The ladder is a series of rectangles all using the same variable to scroll down the screen (offset vertically to give the appearance of being the same rungs scrolling down), which resets when the middlemost rung (the one using dropY as raw input) hits a point offscreen, resetting the group.

[The Star] - The star is comprised of two elipses - one circular and one lozenge - and uses a separate variable for downward movement, and a random dropX variable for its 'spawn'(see: reset)point. This... does not work that well. Sometimes it disappears (I think it's behind the left leg of the ladder??) and falls in the same place twice in a row FREQUENTLY.
Again, Would that I were able, a different piece would have gone here. Oh well.

SELECTION #4
Touchdesigner - Week #8 Exercise #2

['Marble']
This piece looks so cool to me and I almost want to make it into a tileable background. Coloured like something out of The Matrix, its fluid surface and odd-shape really just speak to me.

To break it down:

[The shape] - First using a circle, then lens distorting, then using a normalmap to find the edges, then feeding this into a chromakey TOP. This gave me some lovely little lines to work with. 
Beside this, I made a rectangle, used a circular ramp to get that nice green colour on the edges and a black circle in the center, which I then scaled up in a transform TOP. I composited these two images over one another and transformed them to rotate counter-clockwise, which I then fed through a projection TOP (I love these) set to a fisheye output to make it back into a circle. This I then tiled, reflecting it on the X and Y axes, and fed back through a Fisheye projection TOP to make it a circle again. 

SELECTION #5
Touchdesigner - Week #8 Exercise #3

[Untitled]
Adore the colours in this piece, and the tangibly smoky texture that it carries using the background. This was a joy to make and was also quite a simple process.

To break it down:

[The Background] - Firstly using a circle (that is actually a 7-sided polygon), I fed it down two separate paths through different coloured ramps, and then each through its own projection TOP set to fisheye, animated via absTime.seconds*10/-10 in the rotate X parameter. These were then comped over eachother as well as a black rectangle TOP which served as a background. I then fed this comp through a bloom TOP, and finally fed it through a crop TOP (lol) to get rid of the circular bordering.

[The 'Nails'] - This is a circle (that is actually a 3-sided polygon) which I fed through a projection TOP to get a kind of shark-tooth shape, which I fed into a transform TOP to tile it horizontally and extend the shape out into a nail. I then put this into a ramp TOP to give them red tips and gray heads.
All together - I then comped these two elements together using the Difference operation, which gave this delicious result.

SELECTION #6
Touchdesigner - Week #10 Exercise #1

['Meatcones']
Yeah this looks gross. Love it.

To break it down:

[The Material] - For this, I MovieFileIn TOPped the 'Mettler.2.jpg' image, and fed this alongside a medium-exponent, animated, noiseTOP, into a Displace TOP. This was then tiled, and put into a Null TOP to be fed into a PHONG, skinning my lovely lampshades. 

[The Cones] - Started with a tube SOP turned into a 'lampshade' (radiusA 0 radiusB 2), which was then fed through a twist SOP to give it drillbit-like ridges. Beside this, I created a grid, put it through the ringer with a twist SOP, and then fed this into a noise SOP. This was then used as an Instance reference in the Lampshade's Geometry's 'Instances' parameter.  This resulted in a MESS of cones flying about.
I then transformed this harrowing scene and added a maroon baackground, and recorded a MOV (whoops), which I later had to re-record into a GIF. V happy with this.



