
## ROS_Examples软件使用方法
###0. 安装“noetic”版本ROS
略
###1. 建立ROS工作空间文件夹
例如新建“catkin_ws”文件夹和“src”子文件夹
```sh
mkdir -p catkin_ws/src
```
###2. 将源代码放入“src”文件夹<br>
可以手动复制放入，例如将“helloworld”例程文件夹放入“src”文件夹<br>
也可以从GitHub克隆整个软件到“src”文件夹
```sh
cd ~/catkin_ws/src
git clone https://https://github.com/wanli-car/ROS_Examples.git
```
###3. 安装所需要的依赖
```sh
rosdep install --from-paths src --ignore-src --rosdistro=noetic -y
```
###4. 编译
在“catkin_ws”文件夹目录下执行编译指令
```sh
catkin_make
```
###5. 刷新环境
```sh
source ~/catkin_ws/devel/setup.bash
```
###6. 使用VSCode打开工程（可无）
```sh
code .
```
###7. 启动ROS内核
重新打开一个终端输入
```sh
roscore
```
###8. 运行
在原来的终端中输入
```sh
rosrun helloworld helloworld_node
```
