# Fire and Smoke Tracking and Detection using YOLOv8
## Introduction

This repository contains the code for tracking and detecting fires and smokes in real-time video using YOLOv8. The project uses a pre-trained YOLOv8 model to identify the presence of fire and smoke in a given video frame and track it through subsequent frames. 



https://user-images.githubusercontent.com/22887323/216410880-297f4408-8d22-47a1-b894-6f3f3d8109fb.mp4


## Evaluation
The below chart show  the loss , mAP (mean Average Precision) score for the train, test,validation set.

![alt text](/runs/detect/train/results.png)

### confusion Matrix : 
![alt text](/runs/detect/train/confusion_matrix.png)

##  Inference 
Run the  model using below command:

`!yolo task=detect mode=predict model=<path to weight file> conf=0.25 source=<path to source image or  video> save=True`

The --source argument is required to specify the path to the input video. the above command save your weight in run/predict, which will contain the annotated frames with fire and smoke detections.

## Result
![alt text](/runs/detect/train/val_batch0_pred.jpg)

The project can detect fire and smoke in real-time video with high accuracy. The detection and tracking performance can be improved by fine-tuning the YOLOv8 model on a custom dataset.
It can be used as a starting point for more advanced projects and can be easily integrated into a larger system for fire and smoke monitoring.


## References

- [YOLOv8 paper](https://arxiv.org/abs/2004.10934)
- [YOLOv8 PyTorch implementation](https://github.com/ultralytics/yolov5)
- [YOLOv8 weights conversion script](https://github.com/ultralytics/yolov5/blob/master/weights/convert.py)

