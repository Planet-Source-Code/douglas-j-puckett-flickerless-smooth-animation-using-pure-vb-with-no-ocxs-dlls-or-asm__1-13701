Flickerless, Smooth Animation using pure VB with No OCXs, DLLs, ASM for DirectX!

Just run the demos provided to see the what can be done and then view it's code in the zip files provided.

New - Added a complete ScreenSaver Example!  Fully Functional.  Also fixed the demos for resolution of 1280x1024.
Added Geometry Demo - another example of how to perform this type of animation.

Theres is a total of 4 demos now for you to view (one is a screen saver).

 These demos contain the same methods I use in all of the screensavers I write.  The code included is pure VB code (with just a few APIs declared and utilized). 

Most of the demos contains a bar at the top to change the speed and end the demo.

Most of the code is in the "CodePage.Bas" module.  This contains all of the initialization, variable definitions and declarations and animation code.  The "MainForm.frm" just contains code that will shut down the program when a mouse is clicked or a key is pressed.  There are comments on most of the code.  If there is a real interest in this subject, I may do an indepth explanation of all of the processes involved here, but for now the code comments will have to do.

I use a type I created called Critter.  The Critter type is basically setup to be a sprite.  I have many properties I can set.  I create sprites by declaring an array of critters.  I'm not going to get to technical here but this makes it easy to manipulate many sprites.

Sprites are placed on the screen with a transparent background.  The graphics utilize a mask for the transparancy.  The actual graphics are in one picture loaded into the workpage form.  This graphic contains all of the pictures and their masks.  To make these, you will need to know a bit about using paint programs but that's a whole other ballgame.

The secret to performing animation like this demo uses is to first use a couple of picture boxes as buffers.  One holds a backup image of the background (Clean Screen).  The other picture box is the work screen where all of the graphics are assembled out of sight (WorkScreen).  Once all of the graphics are updated, the individual sprites are then copied to the mainform form for viewing.  After this, the screen is reset by grabbing the same areas where the sprites sit from the "CleanScreen" and pasting the clean areas back to the main screen.  The sprite positions are then moved to new positions and the process starts over again.

The real secret to the speed of this method is not to manipulate whole screens.  I only manipulate the areas of the screen I want to change which greatly increases speed.  Since I use this code in my screensavers, I make sure that the processor utilization stays low and everything runs smoothly.  This code does just that (as long as you don't over do it :).

I will include more examples if there is enough interest in this code.  I will also provide an example screensaver at a later time.  But for now, check out the code and run the examples I've provided.   If you like it, give me a vote or two. 

Demos included are...

Demo_BouncingBalls.exe - About 30 colored balls bouncing all around the screen (Source included).
Demo_BouncingSantas.exe - Bunches of little Santas practicing thier jumping for the upcoming holiday season. 
Demo_Geometry.exe - All kinds of geometric shapes floating around the screen.
Demo_UFO_ScreenSaver.Scr - An alien invasion of UFO's have taken over your screen.  Shows some of the speed of the graphics

 Thanks.   Doug Puckett ( dpuckett@thelittleman.com )

