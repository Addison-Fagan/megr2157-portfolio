# A7 – [Topic]

## Objective
The objective of Assignment 7 was to perform a Finite Element Analysis (FEA) on the bracket design from Assignment 5 using SolidWorks Simulation. A 600 lbf load was applied to evaluate structural performance, and mesh refinement was conducted to ensure result convergence and accuracy. Based on the findings, the bracket was subsequently redesigned to enhance both strength and stiffness.

## Outer Loop 1
Static Stress Analysis
______
A static stress study was initialized in SolidWorks Simulation to evaluate the baseline structural performance of the original bracket design. The component material was assigned as 6061 Aluminum alloy.

Fixtures and Constraints:
Fixed boundary conditions were applied to the upper U-shaped mounting section to fully constrain the bracket, while the lower cylindrical boss remained free to transfer the applied test load.

Applied Loading:
A downward load of 600 lbf—specified in Assignment 5—was applied to the cylindrical section. This setup modeled the tensile loading exerted by a strap pulling directly on the lower cylinder.

Mesh Selection:
A solid tetrahedral mesh was generated using standard default settings. An initial study was executed to establish baseline values for maximum von Mises stress and resultant displacement.

____


A solid mesh was generated for the bracket. First, default mesh settings were applied to establish baseline values for von Mises stress and resultant displacement. For the second mesh, a moderately refined setting was used to evaluate whether the stress and displacement values converged within the required 7 percent threshold. Finally, the mesh density slider was set to the maximum fine setting to obtain final comparison values.

Computation

The static stress study evaluated the von Mises stress distribution, resultant displacement, and deformation behavior of the bracket under the applied load using the fixed boundary conditions and specified mesh configurations.

Data Interpretation and Simulation Results

For Mesh 1, the maximum von Mises stress was 1972.0 MPa, the maximum displacement was 30.72 mm, and the factor of safety was 0.14.

For Mesh 2, the maximum von Mises stress was 1982.4 MPa, the maximum displacement was 30.85 mm, and the factor of safety was 0.139.

For Mesh 3, the maximum von Mises stress was 2289.0 MPa, the maximum displacement was 31.35 mm, and the factor of safety was 0.12.

A. Safety Factor

The material yield strength was 275.8 MPa. The safety factor was calculated using the equation SF equals yield strength divided by maximum von Mises stress. Because the resulting values fell significantly below 1.0, the induced stress substantially exceeded the material yield strength. This indicates that the original bracket geometry is inadequate for the applied load and experiences severe yielding under operating conditions.

B. Maximum Stress and Location

In Mesh 2, the maximum von Mises stress was 1982.4 MPa. This peak stress occurred at the sharp reentrant junction connecting the upper U shaped section to the vertical rectangular support web.

C. Maximum Displacement and Location

In Mesh 2, the maximum resultant displacement was 30.85 mm. This displacement occurred at the free tip of the lower cylindrical strap holder, where the cantilever bending moment was greatest.

Error Estimation and Mesh Validation

Three mesh refinements were evaluated. Comparing Mesh 1 to Mesh 2 showed a stress difference of 0.53 percent and a displacement difference of 0.42 percent. Comparing Mesh 2 to Mesh 3 showed a stress difference of 15.47 percent and a displacement difference of 1.62 percent.

Resultant displacement satisfied the 7 percent convergence limit across all three tests. For stress convergence, Mesh 1 to Mesh 2 met the 7 percent threshold, but Mesh 2 to Mesh 3 failed at 15.47 percent. Because displacement converged while localized stress continued to rise significantly at the finest setting, this demonstrates that peak stress is highly mesh sensitive. This behavior points to a numerical stress singularity caused by the sharp, unfilleted internal corner, where decreasing the element size drives calculated local stress higher rather than converging.

Design Optimization

Reviewing these results highlights two key design modifications required to lower peak stresses and achieve proper convergence.

First, generous blend fillets should be added to the vertical support transitions. Adding fillets to the junctions between the vertical web, the upper U bracket, and the cylindrical boss will smooth the load path and eliminate the artificial stress singularity.

Second, the cross sectional thickness of the vertical support web should be increased. Increasing the web thickness will raise its section modulus and bending stiffness, directly lowering the high bending stresses and significantly reducing the 30.85 mm tip displacement.


## Conclusion 

This assignment demonstrated the practical utility of Finite Element Analysis in pinpointing critical failure modes and localized stress concentrations prior to component fabrication. It also emphasized the direct influence of mesh refinement on simulation fidelity. While displacement fields remained stable across iterations, localized stress values exhibited significant mesh sensitivity due to the sharp geometry of the vertical support. Evaluating these convergence percentages underscored the necessity of mesh refinement studies in diagnosing structural deficiencies and guiding geometric optimization before finalizing a design

this assignment took me 4 hours to complete

