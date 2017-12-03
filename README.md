# Vision submodule for COGROS:Perception

The 'Vision' submodule will emulate human vision. It will allows robots to percieve as humans do.

At the moment, this project is a real-time object recognition application. It does so by using [Google's TensorFlow Object Detection API](https://github.com/tensorflow/models/tree/master/research/object_detection) and [OpenCV](http://opencv.org/).

The detected objects are classified using labelled bounding boxes, but a tracker will save the corresponding pixels in a dynamic memory for the 'Perception' and 'Memory' module.

In the future: 

Vision: Detection - Recognition

When it detects a face:
-then recognize identity
-sentiment analysis: 
-Blink Detection: blink rate
-visual attention detection (gaze tracking): 
-position: face sideways, tilted ?
-age ?
-describe image ?

![](https://github.com/blackvitriol/cog-vision/blob/master/vision2.gif?raw=true)


## Getting Started

   `python object_detection_app.py`
   
 Optional arguments (default value):
 - Device index of the camera `--source=0`
 - Width of the frames in the video stream `--width=480`
 - Height of the frames in the video stream `--height=360`
 - Number of workers `--num-workers=2`
 - Size of the queue `--queue-size=5`

## Tests
```
pytest -vs utils/
```

## Requirements
- [Anaconda / Python 3.5](https://www.continuum.io/downloads)
- [TensorFlow 1.2](https://www.tensorflow.org/)
- [OpenCV 3.0](http://opencv.org/)

## Notes
Using Windows x64 at the moment of deployment.

## Credits/Copyright:

Object Detection:
-https://github.com/datitran/object_detector_app
-See [LICENSE](LICENSE) for details.
-Copyright (c) 2017 [Dat Tran](http://www.dat-tran.com/).
