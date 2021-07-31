# People Counter Solution

This is a Computer Vision Application that counts the number of people entering and exiting a building.

![Demo](/demo/Demo.gif)


## How did we solve this?
As required, we had to train the model on the videos that were provided. Sample images were also obtained from [here](https://drive.google.com/file/d/1LpdHUv5fx4Lbaa_CqMGGeokAZ29neekH/view?usp=sharing)
This people counter implementation uses object detection at fixed frame intervals and uses object tracking the rest of the time. The whole project is implemented in Pyton 3.
A more detailed way of how we solved this problem would be stated in the report



## Object Detection
	
The object detection is done by using YOLO_v3 implemented with openCV2. Normally Yolo v3 is very fast when implemented through darknet (Approximately 30fps), but when implemented using opencv it goes down to a mere 3-5fps. Hence object tracking has been added to speed things up a bit.

## Object Tracking
	
Object tracking here is done using dlib library which keeps track of the objects in the frame by calculating the distances of new estimated positions of the objects(estimated from previous frame) from the positions in the previous frame and saving the same id for the one having minimum distances.


## What you need
	
In order to have the code up and running, the following need to be installed
- OpenCV2
- numpy
- scipy
- dlib
- imutils
- pandas
- cmake
##### This can be done by running the command below since all requirements have been added to a requirements.txt file
    pip install -r requirements.txt
    

# After all libraries are installed,the code can now be run.
##### Run the code below to input a video
    python counter.py --video [full path of the video file]
###### Below is an example of running the code with a local video
    python counter.py --video videos/1.avi
##### If you want to use web cam : 
    python head_count.py  


	

 
