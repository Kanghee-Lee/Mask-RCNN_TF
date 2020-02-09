# Mask-RCNN_TF
Tensorflow implementation of the Mask R-CNN network proposed in 'Mask R-CNN' paper by Facebook AI Research



This is an implementation of [Mask R-CNN](https://arxiv.org/abs/1703.06870) on Python 3, Keras, and TensorFlow. The model generates bounding boxes and segmentation masks for each instance of an object in the image. It's based on Feature Pyramid Network (FPN) and a ResNet101 backbone.

![image](https://user-images.githubusercontent.com/45263010/74101363-55754c80-4b7c-11ea-8efa-60fa898299eb.png)

# Step by Step Detection

## 1. Anchor sorting and filtering
Visualizes every step of the first stage Region Proposal Network and displays positive and negative anchors along with anchor box refinement.
![image](https://user-images.githubusercontent.com/45263010/74101408-d3395800-4b7c-11ea-8f36-078678b77364.png)

## 2. Bounding Box Refinement
This is an example of final detection boxes (dotted lines) and the refinement applied to them (solid lines) in the second stage.
![image](https://user-images.githubusercontent.com/45263010/74101414-e3513780-4b7c-11ea-94b7-3662bfb3796d.png)

## 3. Mask Generation
Examples of generated masks. These then get scaled and placed on the image in the right location.

![image](https://user-images.githubusercontent.com/45263010/74101417-ed733600-4b7c-11ea-9d14-2bcc77704889.png)

## 4.Layer activations
Often it's useful to inspect the activations at different layers to look for signs of trouble (all zeros or random noise).

![image](https://user-images.githubusercontent.com/45263010/74101421-f5cb7100-4b7c-11ea-94e4-812b5e08d261.png)

## 5. Weight Histograms
Another useful debugging tool is to inspect the weight histograms. These are included in the inspect_weights.ipynb notebook.

![image](https://user-images.githubusercontent.com/45263010/74101425-fcf27f00-4b7c-11ea-9fbe-892b80bd5f85.png)

## 6. Logging to TensorBoard
TensorBoard is another great debugging and visualization tool. The model is configured to log losses and save weights at the end of every epoch.

![image](https://user-images.githubusercontent.com/45263010/74101430-07147d80-4b7d-11ea-8d1c-c6359cf6543f.png)

## 7. Composing the different pieces into a final result

![image](https://user-images.githubusercontent.com/45263010/74101437-11cf1280-4b7d-11ea-8187-9edad0297722.png)

The original code is from "https://github.com/matterport/Mask_RCNN"
