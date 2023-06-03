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

## Topics

### Subscribe

- `/scan` lidarの情報受け取り（ sensor_msgs/LaserScan ）
- `/follow_me/control` follow me 開始・終了のシグナル受け取り ( std_msgs/String )

### Publish

- `/mobile_base/commands/velocity` 制御パラメータ送信 ( geometry_msgs/Twist )
