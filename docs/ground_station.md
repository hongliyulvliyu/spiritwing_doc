# 地面站软件配置与使用

## 1. 环境配置
#### 1.1 安装VS community
- 建议使用2019版本；
- 选择安装QT相关内容；
- 在visual studio installer --“单个组件”页面中，勾选windows 10 SDK(10.0.18362.0)

#### 1.2 安装ros-melodic
- 解压解压ros-melodic-desktop_full202010.rar；
- 双击ros-melodic-desktop_full\tools\setup.exe，点击`install`，等待安装（默认路径安装在C盘，建议安装在C盘）；
- 在桌面通过右键，“新建快捷方式”，输入：
```libzmqlibzmq
C:\Windows\System32\cmd.exe /k "C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\Common7\Tools\VsDevCmd.bat" -arch=amd64 -host_arch=amd64 && set ChocolateyInstall=c:\opt\chocolatey && c:\opt\ros\melodic\x64\setup.bat
```
![新建快捷方式](assets/ground_station/新建快捷方式.png)

- 测试：双击生成的快捷方式，看roscore是否启动成功，成功启动效果如下图所示：
![新建快捷方式](assets/ground_station/roscore成功启动.png)

#### 1.3 依赖项
- 将文件zmqpp.7z解压得到文件夹zmqpp，并将此文件夹放置在`C:\opt\ros\melodic\x64\include`下(如ros没有安装在C盘，需要根据ros实际放置的路径进行修改）；
[点击此处下载 zmqpp.7z 文件](../assets/ground_station/zmqpp.7z)

- - 将文件夹libzmq.7z解压缩，将其中的文件`libsodium.dll`，`libzmq-v142-mt-4_3_4.dll`，`zmqpp.dll`，`zmqpp.lib`，`zmqpp-static.lib`放置在路径`C:\opt\ros\melodic\x64\lib下`（需要根据ros实际放置的路径进行修改）；
[点击此处下载 libzmq.7z 文件](../assets/ground_station/libzmq.7z)

<br>

## 2. 本地配置
- 将本地IP修改为144网段，即`192.168.144.xxx`；
检测：ping 192.168.144.xxx【无人机IP】，能ping通说明链路已经连接

- 将工程`station_pad`放置在E盘下，并修改配置文件`station_pad/src/swarm_ros_bridge/ros_topics.yaml`中的`robot1`的IP，修改为上一步骤中修改的本地IP；`robot2`的IP修改为无人机IP

- 软件配套使用的.rviz文件为：
[点击此处下载 spiritWing.rviz文件](../assets/ground_station/spiritWing.rviz)

如希望打开软件后直接加载rviz的配置文件，则将spiritwing.rviz放置在`C:/opt/ros/melodic/x64/share/rviz/`并把名称改为`default.rviz`

<br>

## 3. 使用步骤

