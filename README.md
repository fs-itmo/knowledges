# Formula Student Driverless Resources
 
This repository is devoted to share resources among all Formula Student Driverless teams as well as all other interested parts developing Software and Hardware for autonomous driving and racing. We believe driverless racing is a hard enough challenge and if we share some of our achievments and resources we can accelerate the development of the whole community. Please feel invited to do a pull request and add any dataset, report, or video that can be interesting for the whole community.  

## Table of Contents:
- [Datasets](#datasets)
	- [The FSOCO Dataset](#fsoco)
	- [AMZ Driverless 2017 Dataset](#amz_driverless_2017)
	- [AMZ Vision 2017 Dataset ](#amz_vision_2017)
- [SW Tools](#sw_tools)
	- [Rosbag Bazaar](#rbb)	
- [Algorithms](#algorithms)
	- [MIT Driverless Computer Vision](#mitcv)
	- [MPCC](#mpcc)
	- [Global Race Trajectory Optimization](#grto)
	- [FSD skeleton](#skeleton)
	- [Python Robotics](#pythonrobotics)
	- [RRT path planning for track exploration](#rrtpathplan)
- [Simulations](#sims)
	- [EUFS Simulation](#eufs_sim)
	- [FSSIM](#fssim)
	- [FSDS](#fsds)
- [Conference Papers & Journal Articles ](#papers)
- [Reports](#reports)
- [Presentations](#presentations)
- [Videos](#videos)
___
<br>

<a name="datasets"></a>
# Datasets
This section is devoted to share data collected in, or related to, Formula Student Driverless Vehicles.

<a name="fsoco"></a>
## The FSOCO Dataset
- Website: [www.fsoco-dataset.com](https://www.fsoco-dataset.com)

- The FSOCO dataset helps Formula Student / FSAE teams to get started with their visual perception system for driverless disciplines.

- FSOCO contains bounding box and segmentation annotations from multiple teams and continues to grow thanks to numerous contributions from the Formula Student community.

<a name="amz_driverless_2017"></a>
## AMZ Driverless 2017 Dataset
- The data can be found in this [link](https://www.dropbox.com/s/7x75ks6vo2npfv3/AMZ_driverless_2017_dataset.bag.tar.gz?dl=0)

- The data comes in .bag format. This is the standard logging format for ROS and it can be easily imported to matlab using available tools. 

- The car reference frame is defined as (front, left, up) and has its origin in the IMU reference frame. All the sensors' data are already aligned with the car. The data is given in International Sytem Units unless otherwise specified.

- The data was collected in an airfiled in the outskirts of Zurich. The ground is mostly flat but there are some curved regions and bumps. There is high grass on the side of the of the road. The day was very sunny.

- In this rosbag one can find the following topics:

  - velodyne_points : Contains the Lidar point returns in a sensor_msgs/PointCloud2 message type. The Lidar is a Velodyne Puck VLP16 and the message are the individual packets sent by the sensor. The position of the LiDAR in car_frame is x= 1.6 m, y= 0.0 m.

  - optical_speed_sensor: Contains ground speed data in a geometry_msgs/TwistStamped message type. This sensor is a Kistler Correvit SFII. The position of this sensor in the car frame is x= -0.41m y= 0.27 m.

  - wheel_rpm : contains the wheel speed data in a geometry_msgs/QuaternionStamped message type. x -> front left wheel, y -> front right wheel. z -> rear left wheel. w -> rear right wheel. The data is expressed in rpm's. The distance to thefront axel is 0.81m, to the rear axel 0.72m, and the track width is 1.2m.

  - imu : Contains the accelerometer and gyroscopes information in a sensor_msgs/Imu message type. This sensor is an SBG ellipse-N. The position of this sensor in the car frame is x = 0.0 m, y = 0.0 m. 

  - gps : Contains the GPS information in sensor_msgs/NavSatFix message type. The data is expressed in degrees for Latitude and Longitude. The sensor is the same SBG ellipse-N used as IMU. 

<a name="amz_vision_2017"></a>
## AMZ Vision 2017 Dataset
  - A Vision dataset taken on fluela driverless with all the details can be found in this [link](https://github.com/grafue/SERVO/tree/master/Examples/ROS)

<a name="sw_tools"></a>
# SW Tools
This section is devoted to share software tools related to or helpful in, Formula Student Driverless.

<a name="rbb"></a>
## Rosbag Bazaar
- The Rosbag Bazaar (RBB) is a tool to index/visualize/manage rosbags on remote storage systems. Additionally it provides a web interface and framework for automated simulations. It is a tool helpful to anyone handling large amounts of rosbags and complex software pipelines in real robots. Find the code in this [link](https://github.com/AMZ-Driverless/rbb_core).

<a name="algorithms"></a>
# Algorithms
This section is devoted to share Algorithms dealing with or related to, Formula Student Driverless Vehicles. They could be Visual pipelines, Lidar, estimation, control, etc..

<a name="mitcv"></a>
## MIT Driverless Computer Vision
- Pytorch pipeline of MIT Driverless Computer Vision. Find all the details in this [link](https://github.com/cv-core/MIT-Driverless-CV-Training-Infra).

<a name="mpcc"></a>
## MPCC
- Model Predictive Contouring Controller (MPCC) for Autonomous Racing developed by the Automatic Control Lab (IfA) at ETH Zurich. Find all the details in this [link](https://github.com/alexliniger/MPCC).

<a name="grto"></a>
## Global Race Trajectory Optimization
- Global Race Trajectory Optimization developed by the chair of Automotive Technology of Technical University of Munich (TUM). Find all the details in this [link](https://github.com/TUMFTM/global_racetrajectory_optimization).

<a name="skeleton"></a>
## FSD skeleton
The FSD skeleton repository, found [here](https://github.com/AMZ-Driverless/fsd_skeleton), is an example framework for the code used on a FSD race car. Based on the autonomous software of fluela and gotthard driverless, the framework is built in ROS, and contains the structure and basic ROS nodes to illustrate how to organise an autonomous software stack. Some features are:
- Easy build management
- Custom aliases
- Launchfiles for FSD missions
- Dependency management

<a name="pythonrobotics"></a>
## Python Robotics
- Python code collection of robotics algorithms, especially for autonomous navigation. A great starting point to explore the main algorithms relevant to mobile robotics and Formula Student Driverless. Find all the details in this [link](https://github.com/AtsushiSakai/PythonRobotics).

<a name="rrtpathplan"></a>
## RRT path planning for track exploration
- Code implementation of RRT-based path planning algorithm suitable for exploration of a trackdrive circuit. Find all the details in this [link](https://github.com/MaxMagazin/ma_rrt_path_plan).

<a name="sims"></a>
# Simulations
This section is devoted to sharing simulations dealing with or related to, Formula Student Driverless Vehicles. This could be vehicle dynamic models, environment models, sensors, etc..

<a name="eufs_sim"></a>
## EUFS Simulation
ROS/Gazebo simulation packages for driverless FSAE vehicles. It features a basic RWD Formula Student vehicle model, dynamic event tracks and highly configurable sensor packages. The repository can be found [here](https://gitlab.com/eufs/eufs_sim).

## FSSIM
AMZ Driverless simulator which can be found [here](https://github.com/AMZ-Driverless/fssim)

## FSDS
Wouldn't it be amazing if you could testing your whole autonomous system, without going outside? [Formula Student Driverless Simulator](https://github.com/FS-Driverless/Formula-Student-Driverless-Simulator) tries to achieve exactly that! FSDS is a community project with the goal to provide an end to end simulation for FS Driverless teams. It simulates all commonly used sensors and can connects with ros. This project has proven itsself during FSOnline 2020 where 4 driverless teams competed.

<a name="papers"></a>
# Conference Papers & Journal Articles 
This section is devoted to share Conference Papers and Journal Articles dealing with or related to Formula Student Driverless vehicles.
- Accurate Mapping and Planning for Autonomous Racing. Leiv Andresen*, Adrian Brandemuehl*, Alex Hönger*, Benson Kuan*, Niclas Vödisch*, Hermann Blum, Victor Reijgwart, Lukas Bernreiter, Lukas Schaupp, Jen Jen Chung, Mathias Bürki, Martin R. Oswald, Roland Siegwart, Abel Gawel. (*The authors contributed equally to this work ). [link](https://arxiv.org/pdf/2003.05266.pdf)
- Optimization-Based Hierarchical Motion Planning for Autonomous Racing. José L. Vázquez*, Marius Brühlmeier*, Alexander Liniger*, Alisa Rupenyan, John Lygeros. (*The authors contributed equally to this work ). [link](https://arxiv.org/pdf/2003.04882.pdf)
- End-to-End Velocity Estimation For Autonomous Racing. Sirish Srinivasan, Inkyu Sa, Alex Zyner, Victor Reijgwart, Miguel I. Valls, Roland Siegwart. [link](https://arxiv.org/pdf/2003.06917.pdf)
- Real-time 3D Traffic Cone Detection for Autonomous Driving. Ankit Dhall, Dengxin Dai, Luc Van Gool. [link](https://arxiv.org/abs/1902.02394)
- AMZ Driverless: The Full Autonomous Racing System. Juraj Kabzan, Miguel I. Valls, Victor J.F. Reijgwart, Hubertus F.C. Hendrikx, Claas Ehmke, Manish Prajapat, Andreas Bühler, Nikhil Gosala, Mehak Gupta, Ramya Sivanesan, Ankit Dhall, Eugenio Chisari, Napat Karnchanachari, Sonja Brits, Manuel Dangel, Inkyu Sa, Renaud Dubé, Abel Gawel, Mark Pfeiffer, Alexander Liniger, John Lygeros and Roland Siegwart. [link](https://arxiv.org/pdf/1905.05150.pdf)
- Redundant Perception and State Estimation for Reliable Autonomous Racing.  Nikhil Gosala∗, Andreas Bühler*, Manish Prajapat∗, Claas Ehmke∗, Mehak Gupta∗,Ramya Sivanesan∗, Abel Gawel, Mark Pfeiffer, Mathias Bürki, Inkyu Sa, Renaud Dubé, and Roland Siegwart. (*The authors contributed equally to this work ). [link](https://arxiv.org/pdf/1809.10099.pdf)
- Design of an Autonomous Racecar: Perception, State Estimation and System Integration. Miguel I. Valls*, Hubertus F.C. Hendrikx*, Victor J.F. Reijgwart*, Fabio V. Meier*, Inkyu Sa, Renaud Dubé, Abel Gawel, Mathias Bürki, and Roland Siegwart. (*The authors contributed equally to this work ). [link](https://arxiv.org/pdf/1804.03252.pdf)
- Design of an Autonomous Race Car for the Formula Student Driverless (FSD). Marcel Zeilinger, Raphael Hauk, Markus Bader and Alexander Hofmann. [link](https://info.tuwien.ac.at/mbader/publications/downloads/zeilinger2017.pdf)
- Path following control for autonomous formula racecar: Autonomous formula student competition. Jun Ni and Jibin Hu. [link](http://ieeexplore.ieee.org/document/7995972/)
- Accurate,  Low-Latency  Visual  Perception  for  Autonomous  Racing:Challenges,  Mechanisms,  and  Practical  Solutions. Kieran Strobel, Sibo Zhu, Raphael Chang and Skanda Koppula. [link](https://arxiv.org/abs/2007.13971)


<a name="reports"></a>
# Reports
This section is devoted to share Reports dealing with or related to, Formula Student Driverless Vehicles.

- Learning a CNN-based End-to-End Controller for a Formula SAE Racecar. [link](https://arxiv.org/abs/1708.02215)
<a name="presentations"></a>
# Presentations
This section is devoted to share Presentations related to Formula Student Driverless Vehicles

- ARWo talks (recordings + slides, 2019 + 2020): [link](https://arwo.hamburg/talks/)
- AMZ driverless FSG Workshop 2019 concept presentation: [link](https://youtu.be/PqP08iOvu1g)
- All talks: FSG workshop 2019 (FSD starters): [link](https://www.youtube.com/playlist?list=PLtuNXpGOPQ_aeLQNxB4rLzfb8uktPABU9)
- StarkStrom Augsburg FSG Workshop 2018 FPGA for image detection: [link](https://youtu.be/PhKWKzQZnZs)
- MunichMotorsports FSG Workshop 2018 mono camera in FSD: [link](https://youtu.be/YWnheNLAhlk)
- AMZ driverless FSG Workshop 2018 concept presentations: [link](https://youtu.be/QCoBw-B_Z_4)
- AMZ driverless FSG Workshop 2017 concept presentations: [link](https://youtu.be/26s4LH97kQE)
- AMZ driverless ROSCON conference: Autonomous Racing Car for Formula Student Driverless [link](https://vimeo.com/236115599)


<a name="videos"></a>
# Videos
This section is devoted to share videos related to Formula Student Driverless Vehicles.

<a name="videos_dv"></a>
## Videos of Formula Student Driverless Vehicles

- KIT driverless funny video before first Formula Student Driverless: [link](https://www.youtube.com/watch?v=oEpU_LmfOcs)
- KIT driverless in action: [link](https://www.youtube.com/watch?v=tzZK_nNyr8A)

<a name="videos_dv_algorithm"></a>
## Videos of Algorithms and Formula Student Driverless Vehicles
- AMZ driverless explaining 2018 perception and estimation pipeline: [link](https://youtu.be/ir_uqEYuT84)
- AMZ driverless explaining 2017 perception and estimation pipeline: [link](https://youtu.be/NpLNJ5kC_G0)
- AMZ driverless displaying trajectory: [link](https://www.youtube.com/watch?v=FbKLE7uar9Y)
- EcurieAix driverless displaying cone detection and trajectory: [link](https://www.youtube.com/watch?v=4ah5aZ09i6g)
- RRT exploration of [FSG'17](https://www.youtube.com/watch?v=jJAjrCig3yE) and [FSG'18](https://www.youtube.com/watch?v=kjssdifs0DQ) trackdrive circuits in Gazebo.v