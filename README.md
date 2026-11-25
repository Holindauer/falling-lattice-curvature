### Prompt:

Create a 3D interactive visualization of this as an HTML file I can share with people and they can run locally. Make it self-contained so they can open it in a browser and use it offline.

Let $\mathbb{Z}^2$ be embedded into the $x,y$ plane in ambient space $\mathbb{R}^3$. Now let the points of that 2D integer lattice be nodes, with a directed edge from the origin to every other node, forming a depth-1 directed acyclic graph. Let the weight of each edge be the distance of its node from the origin. Since the lattice is infinite, show a finite disk and let me adjust its radius.

Now let there be a “gravity” force downward along $z$ in $\mathbb{R}^3$. Hold the origin node in place at the top and let the other points fall down from their start positions at $(x,y,0)$. What I mean by being held taut is that the **length of the position vector away from the origin** reaches its assigned value when the point lands. The actual length of the path it traveled can be different. Show me both lengths for a point I select.

Allow each group of points at the same starting radius to form a ring. Include all the radii that occur in the displayed part of $\mathbb{Z}^2$, including ones like $\sqrt{2}$. I don’t want all the points to fall into the same place in the plane projection. I want each shell to have its own ring, with its points evenly spaced around it and with equal radial spacing between consecutive landing rings. Let me adjust that spacing. Orient the shape with the pinned origin at the top, the smaller rings just below it, and the progressively wider rings farther down.

Give me two options for the final vector lengths:

- **Equal steps:** The final distance from the origin increases by the same amount from one ring to the next.
- **Release weights:** Each point keeps its original edge weight as its final distance from the origin.

If a ring has projected radius $\rho$ and its assigned final vector length is $D$, its landing height should be

$$
z = -\sqrt{D^2 - \rho^2}.
$$

Use ring spacings for which the landing heights exist and the wider rings land farther down. Gravity acts straight down. If a point needs to move sideways to reach its assigned place on a ring, make clear that the ring-spacing rule guides that part of the motion.

Now visualize the shape of the curve as the **position plot of the path the point actually followed** from its start position at $(x,y,0)$ to its lowest point. Let me replay the fall or scrub through it, isolate one shell, and toggle the straight vectors from the origin so I can compare them with the paths.

Then allow for a parameter on the visualization for “curvature of space,” in which the natural length of each edge connecting a point in the lattice to the origin may be lengthened or shortened. Call it **release-sheet curvature** $\kappa$, since what I want to vary is how distance is measured on the original $x,y$ sheet. At $\kappa = 0$, the edge weight should be the usual $\sqrt{x^2+y^2}$. Let me turn on unit-distance contours so I can see how those distances change against the original integer grid.

Have a view on the left which is the 3D view, as well as a 2D view over the $x,y$ plane on the right, so I can see how the curvature and ring spacings look in the natural setting. Let me rotate the 3D view or look at it directly from the side.

In the plane projection, also give me a **dots-only option** where the background goes all black and it just displays the current positions as black dots with thin light outlines so they’re visible. In that mode, hide the grid, axes, rings, labels, vectors, and trails in the plane projection. Keep the 3D view interactive alongside it.