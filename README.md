# SAFE-STEPS
AI-powered assistive tool that employs advanced object detection and depth estimation techniques to help elderly/blind individuals

Problems and Solutions-

1. While performing Object Detection, there was an abundance of  images for classes like people and cars and many underrepresented classes, like puddles which created data imbalance and increased the box loss(how well the predicted bounding box covers an object)
We solved this by finetuning the dataset and adding more relevant images

2. The original labels from COCO dataset in the yolov5 model weren't getting detected properly so we froze the initial layers in the YOLO model so we were finetuning hyperparameters to keep the original labels intact

3. Object Detection seemed to struggle with detecting different types of trash cans, mailboxes, and puddles so additional images were added to the dataset, and the model was trained again.


