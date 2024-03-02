# ZUST-Campus

### Structure

All the sensor measurements in the two experiments and the LiDAR SLAM results are stored in two directories, Experiment No.1 and Experiment No.2, respectively. Both directories contain the same subdirectories. The specific contents of these subdirectories are summarized as follows:

(1) Velodyne: The point cloud data obtained from Velodyne VLP-16 are stored in two formats, the BAG file and the PCD file. When running point cloud data using ROS, the reader can use the BAG files. For visualizing point clouds using the MATLAB code provided, the PCD files are recommended.

(2) Ground Truth: The ground truth data are stored in the TXT files in TUM format. We provide the trajectory sample file to facilitate readers to view the length of the ground truth and the position in the satellite map.

(3) IMU: The IMU measurements are stored in the BAG files. The calibration results are stored in the TXT file.

(4) EVO Result: The evaluation results of the three LiDAR SLAM algorithms. The JPG files display the outputted mapping results and the trajectories of SLAM methods. The APE/RPE result files hold the evaluation results of the LiDAR SLAM method.

(5) Video: The process of collecting data is recorded in an MP4 format video file.

![structure](https://github.com/GPumaLee/ZUST-Campus/assets/160859920/791d931a-94d8-4bd0-9b3f-d8962a3cdfc4)


### Systems

The data-collection system of this research consists of three parts: vehicle platform, ground truth system, and LiDAR SLAM module.

(1) Vehicle platform: A WULING Mini EV car is used as a mobile vehicle to carry various types of sensors and on-board computing devices. A customized mounting bracket is installed on the roof to connect and fix various sensors. The copilot position is fitted with a mounting bracket for the onboard computer, which is used for the main computational tasks of the SLAM module.

(2) Ground truth system: The ground truth system is responsible for collecting the precise position and pose value of the vehicle platform during experiments, which is utilized to quantitatively analyze and evaluate the pose estimation results output by the SLAM system. In terms of hardware, an RTK-supported INS-GNSS module with dual antennas is used. A microcomputer is installed on the roof to run the software of the RTK positioning module.

(3) SLAM module: The SLAM module is responsible for running the SLAM method in real-time so that the utility of the dataset can be verified in real-time as the data is collected. The hardware of the module is composed of LiDAR, IMU, and a high-performance PC. The IMU is fixed at the bottom of the LiDAR bracket; The onboard PC is placed in the copilot seat. The proposed method [1] is used to jointly calibrate the LiDAR and IMU. The software part of the SLAM module is implemented based on C++ language under the Robot Operating System (ROS) in Ubuntu 20.04.

![车载系统](https://github.com/GPumaLee/ZUST-Campus/assets/160859920/d8a671df-89dc-46e4-82f7-f59850471d8b)
