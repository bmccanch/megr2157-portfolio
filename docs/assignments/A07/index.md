# A7 – FEA on Bracket

## Design 1 (Outerloop 1)  

This design is the exact same as my Deflection design from A6. The first thing I did for this design was to fixture it so that it can be correctly evaluated using FEA. I fixed the two geometries that would support the most weight in the design. I then added a distributed load on the top half of the cylinder to approximate the loading given by the strap. The image of these fixtures are shown below.
![Fixed geometries and load case](Fixtures.png)

### Innerloop 1
I created the first mesh and ran the analysis for it.

![Design 1, Mesh 1](D1M1.png)
![Design 1, Stress 1](D1S1.png)
![Design 1, Deflection 1](D1D1.png)

For this first mesh, The max stress was 3.044e8 N/m2, which gives a safety factor of 3.0441, and a max deflection of 0.003918". This mesh had 3159 elements.

### Innerloop 2
I then created a finer mesh and ran it.

![Design 1, Mesh 2](D1M2.png)
![Design 1, Stress 2](D1S2.png)
![Design 1, Deflection 2](D1D2.png)

This mesh gave a max stress of 2.78e8 N/m2, which gives a safety factor of 2.98, and a max deflection of 0.003981". This mesh had 7132 elements. For this change, the stress diverged with a difference of 8.67%, and the deflection converged with a difference of 1.60%

### Innerloop 3
I then moved to a third, even finer mesh and ran it.

![Design 1, Mesh 3](D1M3.png)
![Design 1, Stress 3](D1S3.png)
![Design 1, Deflection 3](D1D3.png)

This mesh gave a max stress of 2.95e8 N/m2, which gives a safety factor of 2.8, and a max deflection of 0.003993". This mesh had 26551 elements. For this change, the stress converged with a difference of 6.12%, and the deflection converged with a difference of 0.30%

## Design 2 (Outerloop 2)

Looking at the design 1 and the areas of high stress, I know I need to add a way to decrease stress where the cylinder holder meets the body of the bracket, as well as a way of making the cylinder holder stiffer laterally so that the cylinder doesn't deflect as much. I also want to lower weight, and I plan to do this by hollowing some of the parts out.  

Here is a screenshot of the improved design.
![Design 2 with cutouts and weight savings](Design2.png)

### Innerloop 1
I created the first mesh and ran the analysis for it.

![Design 2, Mesh 1](D2M1.png)
![Design 2, Stress 1](D2S1.png)
![Design 2, Deflection 1](D2D1.png)

For this first mesh, The max stress was 3.06e8 N/m2, which gives a safety factor of 2.7, and a max deflection of 0.0195". This mesh had 30809 elements.

### Innerloop 2
I then created a finer mesh and ran it.

![Design 2, Mesh 2](D2M2.png)
![Design 2, Stress 2](D2S2.png)
![Design 2, Deflection 2](D2D2.png)

This mesh gave a max stress of 3.08e8 N/m2, which gives a safety factor of 2.7 and a max deflection of 0.01954". This mesh had 37821 elements. For this change, the stress converged with a difference of 0.6%, and the deflection converged with a difference of 0.2%


### Innerloop 3
I then moved to a third, even finer mesh and ran it.

![Design 2, Mesh 3](D2M3.png)
![Design 2, Stress 3](D2S3.png)
![Design 2, Deflection 3](D2D3.png)

This mesh gave a max stress of 3.06e8 N/m2, which gives a safety factor of 2.7, and a max deflection of 0.0196". This mesh had 55961 elements. For this change, the stress converged with a difference of 0.6%, and the deflection converged with a difference of 0.31%


## Design 3 (Outerloop 3)

After creating and analyzing the second design, I realized that the main issue was with the stiffness of the main lower bar and the stress concentration at the internal fillet. Because of these, I chose to add a web to the bottom bar to make it into a stronger I-beam type configuration. I also removed more material from the side bars and added a hole in the top bar to make the part lighter as well. Even after adding webbing, the part only weighed 0.200 lbs Because of the other weight savings found.

Here is a screenshot of the improved design.
![Design 3 with cutouts and weight savings](Design3.png)

### Innerloop 1
I created the first mesh and ran the analysis for it.

![Design 3, Mesh 1](D3M1.png)
![Design 3, Stress 1](D3S1.png)
![Design 3, Deflection 1](D3D1.png)

>>>>For this first mesh, The max stress was 3.06e8 N/m2, which gives a safety factor of 2.7, and a max deflection of 0.0195". This mesh had 30809 elements.

### Innerloop 2
I then created a finer mesh and ran it.

![Design 3, Mesh 2](D3M2.png)
![Design 3, Stress 2](D3S2.png)
![Design 3, Deflection 2](D3D2.png)

>>>>This mesh gave a max stress of 3.08e8 N/m2, which gives a safety factor of 2.7 and a max deflection of 0.01954". This mesh had 37821 elements. For this change, the stress converged with a difference of 0.6%, and the deflection converged with a difference of 0.2%


### Innerloop 3
I then moved to a third, even finer mesh and ran it.

![Design 3, Mesh 3](D3M3.png)
![Design 3, Stress 3](D3S3.png)
![Design 3, Deflection 3](D3D3.png)

>>>>>>This mesh gave a max stress of 3.06e8 N/m2, which gives a safety factor of 2.7, and a max deflection of 0.0196". This mesh had 55961 elements. For this change, the stress converged with a difference of 0.6%, and the deflection converged with a difference of 0.31%

## Summary Table

After taking the analyses that converged, the designs resulted in the following:

![Summary Table](Table.png)


