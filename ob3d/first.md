[Previous: Introduction](intro.md)

# 1. Your first OpenB3D program

You've just reached the first (well, actually the second) part of your FreeBasic + OpenB3D journey. In this part, you program your first 3D scene.

### The code

Fire up your editor and enter the following code:

	#include "openb3d.bi"
	#include "fbgfx.bi"

	Using FB

	ScreenRes(800, 600, 32,, GFX_OPENGL)
	Graphics3D(800, 600, 32)

	Do
		UpdateWorld()
		RenderWorld()
		
		Flip()
	Loop Until MultiKey(SC_ESCAPE)

### Compiling and running

Save the file as `first.bas` into your working directory and open the command prompt. Navigate to your working directory you created earlier. If your working directory path is `C:\Users\YOUR_USERNAME_HERE\openb3d\`, for instance, enter `cd openb3d`. Now run `fbc first.bas`. If you followed all of the previous steps there should be no errors. Now launch the executable via the command prompt or just double-click it in Explorer.

You should see something like this:

![Empty black screen](../img/ob3d_1.png)

### What kind of joke is this?

It is not a joke. Yes, it's just a black screen, and yes, it's pretty boring right now. But: It's a working 3D scene, we just haven't added anything yet.

You might ask what the point of this program is. Well, it's supposed to show you the very basic structure of any OpenB3D program without any unneccessary code.

### What does the code mean?

Now we will break the code into small bits and examine it line by line.

	#include "openb3d.bi"
	#include "fbgfx.bi"

What we are doing here is the including of our OpenB3D header file we downlaoded before. Sometimes it's very helpful to take a look at the code contained in this header file, whether you want get a quick overview of the available OpenB3D subs/functions or if you forgot what parameters a function has or what data type its return value has.

The other header file we include is `fbgfx.bi`. This is the header file for the FreeBasic Graphics Library (Gfxlib) which contains constants used in graphics programming.

These two files are the ones you'll always want to include into your programs.

	Using FB
	
As the Gfxlib's constants namespace is `FB`, you would have to call them with their namespace everytime you use a constant. With this line, we can access these constants without the `FB.` prefix.

	ScreenRes(800, 600, 32,, GFX_OPENGL)
	Graphics3D(800, 600, 32)
	
Now it gets interesting: In the first line, we call the `ScreenRes` function. It'll initialize a graphics mode with a display width of 800, a height of 600 and a color depth of 32 bits per pixel. Please note the `GFX_OPENGL`. Here, we initialize OpenGL, the Open **G**raphics **L**ibrary used by OpenB3D. In case you're wondering, we can omit the fourth parameter as we use the default value, hence the two non-separated commas.

The second function call is the first OpenB3D function we use: `Graphics3D`. It sets a 3D graphics mode for our program, and it's *always* the first OpenB3D function to call. The structure of the first three parameters is the same as in `ScreenRes`, so we can use the will arguments as well.

	Do
		UpdateWorld()
		RenderWorld()
		
		Flip()
	Loop Until MultiKey(SC_ESCAPE)
	
What you are seeing here is nothing less than the loop where the 3D scene is updated and rendered (until you either press `Esc` on your keyboard or the program is ended in some unexpected way).

to be continued...

[Next: A light, a camera and a cube](basic.md)