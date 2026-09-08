# A3 – Parametric and FEA

## Objective

The objective for this week's assignment was to design a beam using axial deflection modeling, along with parametric design to determine the beam's length. From this point, the beam should be analyzed using FEA after using parametric modeling to compare the differences in calculated and actual deflection. This introduced me to both parametric modeling and FEA in an effective way.

## 1. Parametric Design
### a.
I started this process using algebra on paper to ensure I had the correct known and unknown values, and to rearrange the axial deformation formula into a format that would allow me to solve for length instead. I also chose my cross-sectional area at this point

[Paper calculations for axial deformation/length](Sketch.png)

### b.
From this point, I plugged these values into Solidworks as my CAD software of choice. I used the "Equations" drop-down menu and entered the variables as shown below. This process was simple and intuitive once I located the equation menu.

[Equation menu drop down](Equation_dropdown.png)

[Variables within equation menu](Equations.png)

### c.
After inputting these variables, I was able to start my model with a sketch of a circle with the correct diameter. The Sigma next to the dimension is the notation that Solidworks uses to denote that a dimension is modeled by an equation or variable.

[Picture of starting sketch](Sketch_radius.png)

The next step after creating this sketch was to extrude it into a three-dimensional beam. I did this using a simple extrude function using the length variable created earlier. This is shown in the picture below.

[HERE](https://drive.google.com/file/d/10803vo6UdBYi4LWc-1cfQo_2aXhEMDo-/view?usp=sharing) is the link to my CAD file.

[Picture of extrude](Extrude.png)

## 2. Finite Element Analysis

After this was completed, I was able to start my FEA simulation. I first started by constraining one end of the beam and applying an axial load to the other end of the beam. The first picture below shows the constraint, and the second image shows the force applied.

[Picture of fixed geometry](Fixture.png)

[Picture of axial force application](Force.png)

After this, I created a mesh for this bar using a rather course element size because of the uniformity and symmetry of the cylindrical beam. I assumed because of this symmetry and the simple geometry (as well as simple load-case) of the beam, a low number of elements would be sufficient to analyze the stresses and deformation for this beam. This mesh is shown below.

[Picture of mesh created for the bar](Mesh.png)

After the mesh was created, the simulation was able to be computed. This gave me both the stress and deformation maps. The deformation map is shown below.

### a.
[Deformation map](Displacement.png)

The map above shows the deformation of the beam. The maximum deformation shown in the beam is _____ . This is ____ percent error compared to the calculated value of ____. 

### b and c.
[von Mises Stress map](Stress.png)

The maximum stress shown in this map is ____ . This maximum stress can be used to determine the safety factor compared to the yield strength of the aluminum alloy I selected. This safety factor can be calculated as ____ . This shows that the force applied on the aluminum is well within the elastic deformation region of a stress-strain curve, and therefore the beam should not plastically deform.

## 3. Design Reflection

### a.
The difference between the calculated deformation (____ in.) and the value found by FEA (____ in.) is ____. The percent error is ___. This is likely from ____. I would trust the FEA more than the simple hand calculation for this situation. the hand calculation is very simplified and assume a lot about how the force is applied. FEA makes fewer assumptions and therefore has a more accurate model.

### b.
HOLE ????

## 4. Lessons Learned
Through this assignment I learned how to create a simple parametric model, as well as some basic fixturing and force application to compute a FEA simulation. This took me about 3 hours to complete because my software and design did not give me any issues or trouble.

## 2157 Section

For this section, I decreased the radius of the beam to a radius of 3/8s of an inch, and increased the force to 400lbf. based on these changes, I believe the beam length will decrease.

