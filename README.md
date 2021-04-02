# Object Counter

Simple program object detction and counting. There are two working modes, in the first it counts the number of objets detected in the scene, in the second only those which cross a given gate. 

For object detction the program uses a [Yolo network](https://github.com/AlexeyAB/darknet). While the demo version comes with a pretrained model that can detect persons, bicycles or cars, you can provide any model trained to detect your custom objects.

<div align="center">
<img src="https://raw.githubusercontent.com/object_counter/master/examples/cars.gif">
</div> 
<br>
<br>

![Alt Image Text](https://github.com/LorBordin/object_counter/master/examples/cars.gif)

## Setup

- Install or build **OpenCV** (building is required for GPU support - recomended). 
- Clone this repo `git clone https://github.com/LorBordin/object_counter`.
- Change directory `cd object_counter`.
- Install  requirements `pip install -r requirements.txt`.

### To use the demo
- Download the Yolo-COCO [weights](https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights) and move them in `models/yolo-coco`.
- run `python demo.py -m counter -v PATH_TO_INPUT_VIDEO`.

**Optional arguments:**
	
  `-m MODE`: *Options: *counter* or *gate_crossing** 	
  `-v VIDEO_PATH`: Path to input video	
  `-y YOUTUBE_URL`: YouTube video URL	
  `-o VIDEO_PATH`: Path to output video		
  `-s 0_or_1`: If 0 doesn't show the live output - deafult 1	                   
  `-l GATE_COORDS`: Gate coords - format: `"[Xt,Yt] [Xb,Yb]"`	
  `-c CLASS`: Object class. Options: *person*, *bicycle*, *car*

### To use your custom weights

Coming soon...