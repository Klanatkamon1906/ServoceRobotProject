# ServoceRobotProject

## Info:
Name:         Natkamon Khantee
Student ID:   62340500018

## How to used this project
# step 0 Setup file 
ตั้งค่าใช้ใช้แหล่งข้อมูลของไฟล์นี้ ให้เข้าไฟล์ทาง terminal ไปจนถึง Kbot แล้วรัน
~~~~~
$ source devel/detup.bash
~~~~~

# step 1 Visualize 
Visualize in Rviz
~~~~~
$ roslaunch Kbot rviz.launch
~~~~~
* การรันไฟล์ใน Rviz จะรันตรงๆไม่ได้ ต้องประกาศเฟรมให้กับโมเดลว่าใช้เฟรมไหนเป็นเฟรมอ้างอิง แล้วค่อยทำการเพิ่ม robot model เข้ามา
~~~~~
$ rosrun tf static_transform_publisher 0 0 0 0 0 0 map base_link 50
~~~~~

Simulation in gazebo
~~~~~
$ roslaunch Kbot gazebo.launch
~~~~~

# step 2 Camera view
เปิดภาพที่กล้องโดยใช้คำสั่ง
~~~~~
$ rosrun image_view image_view image:=/Kbot/camera1/image_raw
~~~~~
