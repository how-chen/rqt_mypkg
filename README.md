# rqt_mypkg
Trying to make sense of [Create your new rqt plugin](http://wiki.ros.org/rqt/Tutorials/Create%20your%20new%20rqt%20plugin#Install_.26_Run_your_plugin) from ROS rQT Tutorials. 

## 1. Create your rqt plugin package 
[Create your rqt plugin package](http://wiki.ros.org/rqt/Tutorials/Create%20your%20new%20rqt%20plugin#Install_.26_Run_your_plugin)

Navigate to the source folder within your catkin workspace directory.
```
cd ~/catkin_ws/src
```

Create empty rqt package
```
catkin_create_pkg rqt_mypkg rospy rqt_gui rqt_gui_pycatkin_create_pkg rqt_mypkg rospy rqt_gui rqt_gui_py
```

Edit the package.xml file.
Between the `<export>`  `</export>` tags, add the following:

```
<rqt_gui plugin="${prefix}/plugin.xml"/>
```
