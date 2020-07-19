This figure shows the effect of increasing the number of steps in a Hough circle transform.  

The first panel shows a circle and three regular polygons: a 4-gon, 8-gon, and 16-gon.  

The second panel shows a Hough circle transform with four steps.  Since all the shapes are radially symmetrical with 90° rotations, they all have an equal peak score at their centroids.

The third panel shows a Hough circle transform with eight steps.  Since the circle, 8-gon, and 16-gon radially symmetrical with 45° rotations, they all have an equal peak score at their centroids.  These shapes have a higher score at their centroids than the 4-gon, because it lacks 45° radial symmetry.

The fourth panel shows a Hough circle transform with sixteen steps.  Only the circle and 16-gon are radially symmetrical at this resolution, so their centroids have equally high scores, while the 4-gon and 8-gon have significantly lower scores.

The fifth panel shows a Hough circle transform with 400 steps. The centroid of the circle now has a higher score than all of the other shapes, allowing for the circle to be distinguished even from the 16-gon.

== Licensing ==
{{cc-by-sa-4.0}}