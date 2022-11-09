ROS Navigation Stack
====================

A 2D navigation stack that takes in information from odometry, sensor
streams, and a goal pose and outputs safe velocity commands that are sent
to a mobile base.

 * AMD64 Debian Job Status: [![Build Status](http://build.ros.org/buildStatus/icon?job=Mbin_uB64__navigation__ubuntu_bionic_amd64__binary)](http://build.ros.org/job/Mbin_uB64__navigation__ubuntu_bionic_amd64__binary/)

Related stacks:

 * http://github.com/ros-planning/navigation_msgs (new in Jade+)
 * http://github.com/ros-planning/navigation_tutorials
 * http://github.com/ros-planning/navigation_experimental

For discussion, please check out the
https://groups.google.com/group/ros-sig-navigation mailing list.

### 关于ROS下输出

* lauch启动节点时，加参数 output="screen"

* 头文件

* 打印方式有：

  std::cout << "" ;

  printf("") ;

  ROS_INFO("") ;
  
### 关于spin 和 spinonce

> https://blog.csdn.net/weixin_40215443/article/details/103793316

spin是被动的一直接收信息，spinonce可以通过设置rate和sleep来控制接收的频率。

```c++
ros::Rate loop_rate(10);//接收频率
while(ros::ok())
{
	// can add some function
    ros::spinOnce();
    loop_rate.sleep();
}
```

### 关于节点的句柄设置

>  https://blog.csdn.net/i_robots/article/details/107508346
注意
1.命名空间，不同命名空间下可能有同名的话题，比如“/persons”和“/move_base/topic”
2.话题的类型，不同的消息类型会被存储在topic的不同区域 


### bind函数占位符


>  https://www.cnblogs.com/houjun/p/4802190.html

### 关于障碍物的设置文件

>  https://blog.csdn.net/i_robots/article/details/107508346
注意
1.当一个障碍物都不添加的时候，会导致仿真环境的加载问题

