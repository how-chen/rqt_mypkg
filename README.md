# rqt_mypkg
Trying to make sense of [Create your new rqt plugin](http://wiki.ros.org/rqt/Tutorials/Create%20your%20new%20rqt%20plugin#Install_.26_Run_your_plugin) from ROS rQT Tutorials. 

## 1. Create your rqt plugin package 
The following is largely from: [Create your rqt plugin package](http://wiki.ros.org/rqt/Tutorials/Create%20your%20new%20rqt%20plugin#Install_.26_Run_your_plugin)

Navigate to the source folder within your catkin workspace directory.
```
cd ~/catkin_ws/src
```

Create empty rqt package
```
catkin_create_pkg rqt_mypkg rospy rqt_gui rqt_gui_pycatkin_create_pkg rqt_mypkg rospy rqt_gui rqt_gui_py
```

## Edit the package.xml file.
Between the `<export>`  `</export>` tags, add the following:

```
<rqt_gui plugin="${prefix}/plugin.xml"/>
```

## Create the plugin.xml file
create a plugin.xml file with the following code: 

```
<library path="src">
  <class name="My Plugin" type="rqt_mypkg.my_module.MyPlugin" base_class_type="rqt_gui_py::Plugin">
    <description>
      An example Python GUI plugin to create a great user interface.
    </description>
    <qtgui>
      <!-- optional grouping...
      <group>
        <label>Group</label>
      </group>
      <group>
        <label>Subgroup</label>
      </group>
      -->
      <label>My first Python Plugin</label>
      <icon type="theme">system-help</icon>
      <statustip>Great user interface to provide real value.</statustip>
    </qtgui>
  </class>
</library>
```
# 2. Create a python plugin
Based on the [rQT Python Plugin ROS Tutorial](http://wiki.ros.org/rqt/Tutorials/Writing%20a%20Python%20Plugin)

create src/rqt_mypkg/ inside the rqt_mypkg package directory
```
% roscd rqt_mypkg
% mkdir -p src/rqt_mypkg
```

note: if roscd does not work, 
```
% cd ~/[workspace_name]
% source ./devel/setup.bash
```



