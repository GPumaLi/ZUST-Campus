# ZUST-Campus

### Structure

All the sensor measurements in the two experiments and the LiDAR SLAM results are stored in two directories, Experiment No.1 and Experiment No.2, respectively. Both directories contain the same subdirectories. The specific contents of these subdirectories are summarized as follows:

(1)Velodyne: The point cloud data obtained from Velodyne VLP-16 are stored in two formats, the BAG file and the PCD file. When running point cloud data using ROS, the reader can use the BAG files. For visualizing point clouds using the MATLAB code provided, the PCD files are recommended.

(2)Ground Truth: The ground truth data are stored in the TXT files in TUM format. We provide the trajectory sample file to facilitate readers to view the length of the ground truth and the position in the satellite map.

(3)IMU: The IMU measurements are stored in the BAG files. The calibration results are stored in the TXT file.

(4)EVO Result: The evaluation results of the three LiDAR SLAM algorithms. The JPG files display the outputted mapping results and the trajectories of SLAM methods. The APE/RPE result files hold the evaluation results of the LiDAR SLAM method.

(5)Video: The process of collecting data is recorded in an MP4 format video file.

![structure](https://github.com/GPumaLee/ZUST-Campus/assets/160859920/791d931a-94d8-4bd0-9b3f-d8962a3cdfc4)
