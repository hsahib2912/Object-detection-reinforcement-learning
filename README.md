# Object-detection-reinforcement-learning
The project aims at finding objects in images using stacked networks of YOLOV5 and Dense Q Network.<br/>
Following is the network architecture of the network.
![Screenshot 2021-08-11 at 10 16 56 AM](https://user-images.githubusercontent.com/58325853/128971076-f73897e5-5208-4aeb-bad0-3405c0b80a53.png)<br/>
As show in image above, initially images are passed through the YOLOV5 network to get the list of boxes bounding the objects in images and then that list is feeded into the Deep Q Network. <br/>
Architecture of Deep Q Network follows:
Layer  | Number of nodes
------------- | -------------
Input  | 5
Hidden 1  | 100
Dropout 1 | p=0.2
Hidden 2 | 1000
Dropout 2 | p=0.2
Output | 4 
-----------------
Following attributes are used for reinforcement learning:<br/>
* Environment : Bounding box coordinates.<br/>
* Action : Agent can alter the coordinates of the bounding box.<br/>
* Reward : +1 if IOU > 0.5; else -1<br/>
* State : Output of YOLOV5 model ([x_center, y_center, width, height])
