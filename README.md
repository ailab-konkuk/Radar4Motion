# Radar4Motion: 4D Imaging Radar IMU-free Odometry with RCS-weighted Correspondences
Codes for paper "*Radar4Motion: 4D Imaging Radar IMU-free Odometry with RCS-weighted Correspondences*"

The code and dataset (ROS bag files) will be uploaded after the review process!

## Demo
<img src="./images/lidar_versus_radar.png" width="800">

- **Beige**: 32ch LiDAR Point Cloud
- **Rainbow (bold)**: 4D Imaging Radar Point Cloud

### Trajectory 1 (Urban)
<img src="./images/main.gif" width="800">

### Trajectory 2 (Tunnel)
<img src="./images/tunnel_odom.gif" width="800">

- The above `gif` shows **ONLY** odometry-based mapping results.
    - *NO inertial sensor, NO GNSS sensor, NO loop-closure*
    - **Only Single front-view 4D Imaging Radar!**
        - *yellow* : feature point cloud
        - *red* : submap point cloud
        - *rainbow* : raw radar point cloud
        - *white* : 32ch-LiDAR point cloud

## Dataset
- Format
    - rosbag (*.bag*)
- Data acquired from ***Bundang-gu, Seongnam-si in South Korea*** <img src="./images/real-world.png" width="500">
    - Sensor
        - Bitsensing AFI910, RTK-GNSS(Novatel CPT7), Velodyne 32ch LiDAR, Camera
    - **Available Topics**
        - 4D Imaging Radar: `/afi910_cloud_node/cloud`
        - RTK-GNSS: `/novatel/oem7/inspvax`
        - IMU: `/novatel/oem7/corrimu`
        - 32ch LiDAR: `/velodyne_points`
        - Camera: `/a2A1920/image_raw/compressed`

## Contact

If you have any questions, please let me know:
- Soyeong Kim (`kimchuorok@gmail.com`)

## Acknowledgement

In the development of this package, we refer to [KISS-ICP](https://github.com/PRBonn/kiss-icp) and [REVE](https://github.com/christopherdoer/reve) for source codes.\
We utilized a [evo](https://github.com/MichaelGrupp/evo) package for odometry evaluation.
