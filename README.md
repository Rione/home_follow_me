# follow_me

自己位置推定のアルゴリズムを利用した、精度の高いfollow meのプログラムです。

## Setup

```
cd ~/catkin_ws/src
git clone https://github.com/rione/home_follow_me follow_me
git clone -b noetic-devel https://github.com/ros-perception/laser_filters
cd ~/catkin_ws
catkin_make
```

## Usage

```
roslaunch follow_me follow_me.launch
```

## follow_me_node

### Subscribe Topics

- `/scan` lidarの情報受け取り（ sensor_msgs/LaserScan ）
- `/follow_me/command` follow_me 開始、終了のシグナル受け取り ( std_msgs/String )
    - `start` で開始
    - `stop` で停止

### Publish Topics

- `/cmd_vel` 制御パラメータ送信 ( geometry_msgs/Twist )
- `/follow_me/player_point` オペレーターの予測位置 (std_msgs/Float32MultiArray )
