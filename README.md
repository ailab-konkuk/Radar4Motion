# Rad4Motion: 4D Imaging Radar IMU-free Odometry with RCS-weighted Correspondences

The code and dataset (ROS bag files) will be uploaded by February 2024!

## Demo

<img src="./images/main.gif" width="800">

## Dataset
- Format
    - rosbag (*.bag*)
- Data acquired from ***Bundang-gu, Seongnam-si in South Korea*** <img src="./images/real-world.png" width="500">
    - Sensor
        - Bitsensing AFI910, RTK-GNSS(Novatel CPT7), Velodyne 32ch LiDAR, Camera
    - **Available Topics**
        - 4D Imaging: `/afi910_cloud_node/cloud`
        - RTK-GNSS: `/novatel/oem7/inspvax`
        - 32ch LiDAR: `/velodyne_points`
        - Camera: `/a2A1920/image_raw/compressed`

## Contact

If you have any questions, please let me know:
- Soyeong Kim (`kimchuorok@gmail.com`)

## Acknowledgement

In the development of this package, we refer to [KISS-ICP](https://github.com/PRBonn/kiss-icp) and [REVE](https://github.com/christopherdoer/reve) for source codes.\
We utilized a [evo](https://github.com/MichaelGrupp/evo) package for odometry evaluation.
