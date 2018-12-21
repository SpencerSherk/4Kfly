#4K fly
Check out the NetworkSolo scene (default at the moment) for a fun networked flying bee game. I dropped this in to start getting the hang of networking in unity, which I will need to control the 3D display parameters once it goes full screeen (sliders not nicely visible).
Magic Leap, this would be a nice spin-off from my proposed project, the Vision Assistant.

4K fly generates a few thousand different views of a scene, organized and played back on a hex grid intended to play behind a hexagonal lens array, creating a 3D (NO GLASSES!) display.

The meat of the thing is in NewBehavior.cs, in the Update(). There is a loop there that does camera move, render, copy to slice of texture array. 

I believe modifying gpu-instancing to render each instance to a different slice of the texture array will be the solution for speed up. Somewhere in the scriptable render pipeline, which I have not learned enough about.

cio
