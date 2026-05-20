# Outage Process Details

ICDS engineers have updateed and expanded the outage protocol to improve recovery time and expand testing. 

The outage workflow has been updated to make use of serviceNOW and provide tracking.

 - changes are throughly documented
 - includes a review by leadership to understand potential impacts
 - system test plan that includes client-submitted use cases


![Outage WorkFlow Diagram](../img/ICDS_Outage_workflow.png)

# Rolling Outage Process 

Beginning in March 2026 ICDS will reduce the yearly number of full Roar outages and will instead implement “rolling maintenance” windows. 

During rolling maintenance, the Roar cluster will remain available to users. Small portions of the cluster are taken offline, serviced, and then returned to production, until the entire cluster has been updated. System engineers have utilized these techniques successfully in the past, and ICDS is pleased to expand their use to improve Roar user experience during scheduled maintenance. 

## What Can Users Expect During Rolling Maintenance? 

Compared to a full outage, users can expect much less impact on workflows. Here are some details to keep in mind: 

- Running jobs will continue uninterrupted, and users may continue to submit jobs and access data. 

- Between 5:00-8:00 a.m. on the day of the outage, service nodes will be rebooted, and this could briefly interrupt users’ ability to work with interactive desktop sessions, edit files from submit nodes, or submit jobs. 

- Taking nodes offline in small batches for service does reduce the available cluster resources, and this could result in longer wait times for larger jobs. System performance is monitored throughout rolling maintenance.  


## Post outage test

Post outage ICDS Engineers go through a series of test to show basic connectivity and functionaloty of services (i.e. job submission, Slurm, OOD portal, Globus access, science gateways). This will be followed by application test detailed below. 

Includes sample test for the following applications:

 |         |             |                                 |
 |---      |---          |---                              |---
 | C       | MPI_Testall | bash / Slurm submission testing |
 | comsol  | cpp         | fluent                          |
 | fortran | gpu nbody   | gromacs                         |
 | java    | julia       | mathematica                     |
 | matlab  | py_array    | python                          |
 | r       | starccm     |                                 |

Includes user test for the following applications: 

 - Ansys Fluent job
 - MPI fluid solver
 - Gaussian
 - OpenFOAM
 - COMSOL
 - MATLAB sine_wave 

**Your input is valuable**. At the conclusion of every outage, ICDS engineers run extensive use case tests to ensure that the system will work as expected. If your team runs your own post outage tests or if you have ideas for tests you’d like ICDS engineers to run, [please let us know.](mailto:icds@psu.edu?subject=Post-Outage%20Testing%20Feedback)

 
