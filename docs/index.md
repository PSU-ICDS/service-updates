# Outage Process Details

ICDS engineers have updateed and expanded the outage protocol to improve recovery time and expand testing. 

The outage workflow has been updated to make use of serviceNOW and provide tracking.

 - changes are throughly documented
 - includes a review by leadership to understand potential impacts
 - system test plan that includes client-submitted use cases


![Outage WorkFlow Diagram](../img/ICDS_Outage_workflow.png)

# Rolling Maintenance Process 

Beginning in March 2026 ICDS will reduce the yearly number of full Roar outages and will instead implement “rolling maintenance” windows. 

During rolling maintenance, the Roar cluster will remain available to users. Small portions of the cluster are taken offline, serviced, and then returned to production, until the entire cluster has been updated. System engineers have utilized these techniques successfully in the past, and ICDS is pleased to expand their use to improve Roar user experience during scheduled maintenance. 

## What Can Users Expect During Rolling Maintenance? 

Compared to a full outage, users can expect much less impact on workflows. Here are some details to keep in mind: 

- Running jobs will continue uninterrupted, and users may continue to submit jobs and access data. 

- Between 5:00-8:00 a.m. on the day of the outage, service nodes will be rebooted, and this could briefly interrupt users’ ability to work with interactive desktop sessions, edit files from submit nodes, or submit jobs. 

- Taking nodes offline in small batches for service does reduce the available cluster resources, and this could result in longer wait times for larger jobs. System performance is monitored throughout rolling maintenance periods.  


# Post outage test

Post outage ICDS Engineers go through a series of test to show basic connectivity and functionaloty of services (i.e. job submission, Slurm, OOD portal, Globus access, science gateways). This will be followed by application test detailed below. 

Includes sample test for the following applications:

<table>
  <tbody>
    <tr>
      <td>C</td>
      <td>MPI_Testall</td>
      <td>bash / Slurm submission test</td>
    </tr>
    <tr>
      <td>comsol</td>
      <td>cpp</td>
      <td>fluent</td>
    </tr>
    <tr>
      <td>fortran</td>
      <td>gpu nbody</td>
      <td>gromacs</td>
    </tr>
    <tr>
      <td>java</td>
      <td>julia</td>
      <td>mathematica</td>
    </tr>
    <tr>
      <td>matlab</td>
      <td>py_array</td>
      <td>python</td>
    </tr>
    <tr>
      <td>r</td>
      <td>starccm</td>
      <td></td>
    </tr>
  </tbody>
</table>

Includes user test for the following applications: 

<table>
  <tbody>
    <tr>
      <td>Ansys Fluent job</td>
      <td>MPI fluid solver</td>
      <td>Gaussian</td>
    </tr>
    <tr>
      <td>OpenFOAM</td>
      <td>COMSOL</td>
      <td>MATLAB sine_wave</td>
    </tr>
  </tbody>
</table>

**Your input is valuable**. At the conclusion of every outage, ICDS engineers run extensive use case tests to ensure that the system will work as expected. If your team runs your own post outage tests or if you have ideas for tests you’d like ICDS engineers to run, [please let us know.](mailto:icds@psu.edu?subject=Post-Outage%20Testing%20Feedback)

 
