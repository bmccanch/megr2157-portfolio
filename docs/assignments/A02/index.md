# A2 – Truss Stress Analysis

## Objective

The objective for this assignment is to design a a lightweight truss that would support two separate forces of the same magnitude but in varying directions. The designated attachment points and force locations and directions are given, but no preliminary truss designs are given. The image below is the layout of these attachment points, and the variables are given set values within the body of the assignment
![Image of a pin and a slider connection the truss must be mounted from, and the distances between the attachment points and the forces applied](Assignment.png)

## Analyze

From this description of the assignment objective, I then analyzed the requirements and restrictions given that would change the approach of my design. The biggest of these was the requirement to have a uniform cross-sectional area for each beam, this meant that I could not cater beam thicknesses to the stresses applied to them. Another large restriction was the given safety factor. This factor increased weight drastically compared to a lower value because it requires the cross-sectional area to be much larger.

## Decide

After this analysis, I then started on my design. After brainstorming for some time, I decided that having a symmetrical design would be best suited to this challenge. This would allow for the stresses within the beams to have the most similar magnitudes. From this point I created a design that would allow for the main beams connecting at each force, P, to carry the loads as close to symmetrically as possible. This design is shown below.

![Image of the sketch of the truss with some preliminary calculations](Sketch.png)

I chose to prioritize equal loading of the beams because this allows for the lightest weight design. The large safety factor and uniform cross-sectional area restrictions would not cause the beams to be overbuilt if all of the beams have the same forces through them.

From this point I then continued onto using the geometry from the design to analyze the forces through each beam as shown below (a few equations are also on the image above).

![Image 1/2 of statics calculations done](Statics.png)
![Image 2/2 of statics calculations done](Statics_2.png)

The maximum force through the beams was 22.73 kN of force. This force is not much higher than the applied force of 20kn at P. From here I was able to determine the required cross-sectional area of the beams, as well as the weight of the truss based on the geometry of the truss as well as the material properties of the A36 steel I used (A500 was not available in my CAD software of choice). These calculations are depicted below.

![Image of truss solids calculations done](Truss_solids.png)

After these calculations I then moved onto the pins which were required to be made of tool steel with designated properties. Using these properties along with the forces I found at each connection point, I found the minimum cross-sectional area with the safety factor that was given, as well as the total weight of all four pins combined. These final calculations are shown in the image below.

![Image of pin solids done](Pin_solids.png)

These decisions led me to modelling the following truss and pins as my final design in Solidworks. I did this using global variables so that the size of each component could be changed easily if needed. The images below show both designs once completed. The truss CAD file can be downloaded [here](https://drive.google.com/file/d/1wJ27q34oLm1ofn0M7SDJjOxS56n2aYaU/view?usp=sharing), and the pin CAD file can be downloaded [here](https://drive.google.com/file/d/1J8cG6q1LV1tzHJmihBDEIcMg-gMSjkL5/view?usp=drive_link). The design and calculations took 2 hours, the modeling took 1 hour, and recounting the steps and formatting the assignment took about 4 hours.

![Image of 3D truss model](Truss_render.png)
![Image of 3D pin model](Pin_render.png)

## Communicate

As I completed this project, it made me realize how many choices there are while designing even a simple part. This emphasized the importance of justifying my design decisions as I was making them, as well as documenting the process so that I could defend my choices. This is important because within engineering, all of our choices must be defendable with empirical data, not just anecdotes or "feelings" about what is right. Some creative liberty may be taken, and even encouraged, but it must be clear that your choices still have a solid foundation in engineering principles.

This specific project taught me how to design a part with a safety factor, as well as how to justify my design choices.

## MEGR 2157 Addition
### Part 1: Truss Members

#### Tension Members
Because I am using a milder steel of A36, the expected failure mode would be yielding. This is the case because the material is ductile and would easily plasticly deform compare to a brittle material that may fracture instead. A way to change this would be to increase the surface area of the truss members to an even larger size to reduce the stress traveling through each beam.

#### Compression Members
As earlier stated, this is a mild steel that is rather ductile so buckling due to elastic deformation would be the most likely cause of failure. This could also be remedied by increasing the cross-sectional area or by employing hollow beams with the same area of steel while having a higher resistance to buckling.

### Part 2: Pin Connections

The most likely failure case would typically be bearing yielding or potentially a shear failure. Because the joint is single shear, this means the load on the bearing surface is not uniform and could create high-stress areas within the truss material. Since the pin material is much harder than the truss material, this would make the bearing deformation more likely than shear failure. A simple solution for this would be to implement a simple double shear connection instead. This would allow for a similar weight while being a much stronger joint.

#### Sources:
https://efficientengineer.com/buckling/
https://mechanicalc.com/reference/lug-analysis#simplified-bearing-failure
