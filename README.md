# Object-detection-reinforcement-learning
The project aims at finding objects in images using stacked networks of YOLOV5 and Dense Q Network.<br/>
Following is the network architecture of the network.
![Screenshot 2021-08-11 at 10 16 56 AM](https://user-images.githubusercontent.com/58325853/128971076-f73897e5-5208-4aeb-bad0-3405c0b80a53.png)
As show in image above, initially images are passed through the YOLOV5 network to get the list of boxes bounding the objects in images and then that list is feeded into the Deep Q Network.
