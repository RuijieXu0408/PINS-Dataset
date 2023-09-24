# PINS-Dataset
This repository is the usage page of the PINS-dataset. Since the positioning of GNSS is affected by the multipath effect in complex scenes such as urban canyons, the use of IMUs for positioning has become one of the hotspots in the field of positioning and navigation. Although there are many datasets on IMUs in the current GitHub, there are still fewer datasets on pedestrian navigation systems using foot-tethered IMUs. The data in this dataset are collected from a KERNEL-100 IMU developed by Beijing BDStar Navigation Co., Ltd. in circular flower bed and staircase scenes respectively. The acquisition of this dataset was done by the Parallel Intelligent Technologies and Systems team at the Institute of Automation, Chinese Academy of Sciences.

This repository is dedicated to provide a public dataset for PINS researchers, if you have any questions about using the dataset, please feel free to contact shichao.chen@ia.ac.cn.
## IMU Parameters
<table>
    <tr>
        <td rowspan="2">Accelerometer</td><td>Measuring Range</td><td>2000°/s</td>
    </tr>
    <tr>
        <td>Sampling Rate</td><td>500Hz</td>
    </tr>
    <tr>
        <td rowspan="2">Gyroscope</td><td>Measuring Range</td><td>16g</td>
    </tr>
    <tr>
        <td>Sampling Rate</td><td>500Hz</td>
    </tr>
    <tr>
        <td>communication Mode</td><td>Port</td><td>4~15V RS422</td>
    </tr>
</table>

##  1) Flatland scenario

In this dataset, the sampler walked normally around a circular flower bed with a circumference of about 27.6m, and ended the walking experiment at the same position as the start point so that the start-end position was the same, with a systematic error of about 82mm. The image of this flower bed is shown in Fig. 1. Therefore, the performance of the error correction method can be evaluated based on the error between the end point and the start point of the trajectory after the experimental filtering.

<img decoding="async" src="https://github.com/RuijieXu0408/PINS-Dataset/assets/65544040/975c88ef-2034-4807-acc1-f25dbe0844e1" width="33%">

Fig.1. Circular flower beds (this image was taken from a top view tilted at a certain angle, the actual terrain is square)

## 2) Stairs scenario

This scenario is to test the inertial guidance positioning performance of a pedestrian moving up and down stairs in a scenario with altitude change. The experiment is as follows: the pedestrian walks up two 10-step staircases from the 9th floor to the 10th floor and then returns to the starting point on the 9th floor in the same way. Ideally, after the pedestrian returns to the starting point in the original way, the three-dimensional visualization results resolved by the algorithm in the host computer should also return to the original point, and the simulation image should change along the staircase trajectory. The stairs scenario is shown in fig. 2.

<img decoding="async" src="https://github.com/RuijieXu0408/PINS-Dataset/assets/65544040/d42ad1de-b0a5-4049-8a66-ac93e28a4360" width="33%">

Fig. 2. Stairs field scene experiment

## Description of the data set format

This experiment mainly uses the three-axis accelerometer and three-axis gyroscope of the IMU, the sampling rate is 500Hz, and the samples are shown in Figure 3. The first three columns of data are respectively the x, y, z-axis acceleration data in the process of pedestrian movement recorded in the first three columns; the second three columns of the x, y, z-axis angular velocity movement data in the process of pedestrian movement recorded in the second three columns.

<img decoding="async" src="https://github.com/RuijieXu0408/PINS-Dataset/assets/65544040/85959613-f1c0-4853-9b7b-c918fe1e901a" width="63%">

Fig. 3. The samples of dataset

# Citations

If you use this dataset please cite our upcoming papers:

R. Xu, S. Chen, W. Sun, Y. Lv, J. Luo, Y. Tang, "A SINS Error Correction Approach Based on Dual-threshold ZV Detection and Cubature Kalman Filter," *2023 IEEE International Conference on Systems, Man, and Cybernetics,* Honolulu, Oahu, Hawaii, 2023.

# Acknowledgements

The acquisition of this dataset was done by the Parallel Intelligence Lab at the Institute of Automation, Chinese Academy of Sciences. This work was supported by the Center of National Railway Intelligent Transportation System Engineering and Technology (Contract No. RITS2021KF03,2021YJ004), China Academy of Railway Sciences and CAS STS Dongguan Project (20201600200132).
