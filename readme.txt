                                Copyright (c) 2021 Mankoff Consulting

                    Permission is hereby granted, free of charge, to any person obtaining a copy
                    of this software and associated documentation files (the "Software"), to deal
                    in the Software without restriction, including without limitation the rights
                    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
                    copies of the Software, and to permit persons to whom the Software is
                    furnished to do so, subject to the following conditions:

                    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
                    EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
                    OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFINGEMENT.
                    IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
                    CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
                    TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE
                    OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


 Overview of ScriptJS:
 * I initially set canvas to draw a circle upon each mouse click and add the click event to my global event listener
    assigning it to the mouse object.
 * I declare my function drawCircle after I've added my event listener on click event.
 * Inside my drawCircle function I added x,y event variables so the coordinates of my mouse click get passed to canvas
   and it will draw the circle where I'm clicking.
 *JS only loads from memory so declaring a function is needed to ensure the persistence and allow me to re-use the
    object.
 * I assign my mouse variable to undefined which sets the cursor to only begin drawing once it's moved. If I had set
    it to null or defined a value for it, that would cause drawCircle to immediately begin and would simulate how a
    paintbrush feature on a device using a mouse would look whereas I'm only wanting the brush to begin once the cursor
    begins to move. This is what I will be using to create the mouse interaction to draw the particles.
 * I've set both the X/Y speeds for the particles as positive. This will cause the particles to only move to the right
    from their start position.
 * The class Particle sets additional perimeters for my object and it creates a 2d Vector image via the offset
   negative values I've assigned in my speedX & speedY variables.
 * I've created a simple draw method that tells canvas the coordinates at which it should begin drawing and I've set
   speed coordinates to control the amount of particles being emitted.
