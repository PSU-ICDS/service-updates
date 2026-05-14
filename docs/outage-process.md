# System outages

ICDS engineers have updateed and expanded the outage protocol to improve recovery time and expand testing. 

The outage workflow has been updated to make use of serviceNOW and provide tracking.

 - changes are throughly documented
 - includes a review by leadership to understand potential impacts
 - system test plan that includes client-submitted use cases


![Outage WorkFlow Diagram](../img/ICDS_Outage_workflow.png)


## Post outage test

Post outage ICDS Engineers go through a series of test to show basic connectivity and functionaloty of services (i.e. job submission, Slurm, OOD portal, Globus access, science gateways). This will be followed by application test detailed below. 

Includes sample test for the following applications:

 - C
 - alltest (MPI network latency mapping test)
 - bash / Slurm submission testing
 - comsol
 - cpp
 - fluent
 - fortran
 - gpu nbody
 - gromacs
 - java
 - julia
 - mathematica
 - matlab
 - py_array
 - python
 - r
 - starccm

Includes user test for the following applications: 

 - Ansys Fluent job
 - MPI fluid solver
 - Gaussian
 - OpenFOAM
 - COMSOL
 - MATLAB sine_wave 

**Your input is valuable**. At the conclusion of every outage, ICDS engineers run extensive use case tests to ensure that the system will work as expected. If your team runs your own post outage tests or if you have ideas for tests you’d like ICDS engineers to run, [please let us know.](mailto:icds@psu.edu?subject=Post-Outage%20Testing%20Feedback)

 
