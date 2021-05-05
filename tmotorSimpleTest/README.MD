simple test：  
## 创建简单工作空间

mkdir ~/catkin_ws;cd catkin_ws  
mkdir src  
cd src  
把tmotortest文件夹放到src目录下  
## 编译package

cd ~/catkin_ws  
catkin_make  
source devel/setup.bash  

## 使能串口
sudo ip link set can0 type can bitrate 1000000  
sudo ip link set up can0  
## 运行demo(给电机发送一个正弦位置信号，对电机进行位置环控制)
roscore  
rosrun tmotortest rostest1  

## 注意这部分少了一些关于设置电机id的知识，如果有需要再联系我（代码里面使用的电机id是2，默认电机id是1）
