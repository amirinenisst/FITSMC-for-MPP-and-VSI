# FITSMC-for-MPP-and-VSI


### Reflection
* This thesis presented a complete approach to control the PV grid by controlling the tracking error of boost converter and also
control of voltage source inverter.
* It focused on controlling the tracking error of maximum power point, also mitigating the voltage fluctuations due to faults
raised near the grid and production of stable output by controlling the voltage source converter.
* Fuzzy based approach reduced complex computations by avoiding unnecessary manual tuning of gain constants.
* MATLAB/Simulink is used for modelling the PV grid and the results are obtained to validate the proposed approach.
* Different case scenarios are considered and results are compared with sliding mode control based PV grid outputs to show
the effectiveness of FITSMC.
* FITSMC controller efficiency and ability can be said by its robustness in stability, finite time convergence and less settling
time which are depicted in results.


[//]: # (Image References)
[image1]: ./images/gridmodel.png
[image2]: ./images/algorithm.png
[image3]: ./images/topology.png
[image4]: ./images/case-1.png
[image5]: ./images/case-2.png
[image6]: ./images/case-3.png

### Why PV
Economically optimal size
Easy to design
Abundantly available
Compatibility with utility grid
Extraction and tracking the maximum power
Dynamic performance of a VSI

### Grid-connected PV array block diagram

![alt text][image1]

### Different controllers
* PI controller
* Fuzzy controller
* Adaptive controller
* Sliding mode controller
* Terminal sliding mode contoller
* Fuzzy based integral terminal sliding mode controller

I've choosen Fuzzy based integral terminal sliding mode controller because of its advantages described below

* Less chattering effect
* Less settling time
* Minimum overshoot
* Fast convergence rate
* Robustness under  parametric uncertainties
* Using fuzzy logic only in some parts of control scheme reduces the complexity and enhances the flexibility

### MPP
Out of many algorithms for MPPT I've chosen Perturb and observe and it is shown below
![alt text][image2]

### VSI
Topology of VSI control is shown below
![alt text][image3]

### Results
CASE- 1
Irradiance=1000 W/m2
Temperature=25
Reference voltage=500V
Output voltage of boost converter in case-1 is shown below
![alt text][image4]

CASE-2
Changing Irradiance
Changing Temperature
Output voltages of FITSMC and SMC based boost converters in case-2 is shown below
![alt text][image5]

CASE-3
Changing Irradiance
Changing Temperature
Three phase grid fault from t=0.4sec to 0.6 sec 
Output voltages of FITSMC and SMC based boost converters in case-3 is shown below
![alt text][image6]
FITSMC settling time= 0.7 sec
SMC settling time= unsettled

### Publications
Sai Sree Teja Amirineni, Mohammad Javad Morshed, Afef Fekih, “ Integral terminal Sliding Mode Control for maximum power production in grid connected PV systems” IEEE Conference on Control Applications (CCA) Part of 2016 IEEE Multi-Conference on Systems and Control September 19-22, 2016. Buenos Aires, Argentina.
