# Computer Vision Techniques Using  Classified Systems 
Utilizing  fundamental techniques to detect moving objects in a background subtraction. 
For this implementation, I installed OpenCV and NumPy. 
These systems were most useful for identifying and locating objects. Ideally, an algorithm will not be accurate, especially in environments with rapid changes. Therefore, detection was difficult. A dataset with images of the three object types (cars, bicycles, pedestrians) was used to annotate.
## Deployment
To deploy this project run
```python 3.x version 
   numpy, and OpenCV 2.4.x version
```

## Documentation
[Documentation](https://github.com/Treddd88/Coding-Challenge-.git)

## Dataset
https://designer.microsoft.com/design?skiptoguestmode=true 
## Object Detection 
	To detect objects, a pre-trained deep learning model was used; the YOLO (You Only Look Once) model.
## Process Overview 
	Load an image.
   Convert it to grayscale.
	Apply a Gaussian filter to reduce noise.
	Load a pre-trained object detection model (such as YOLO).
	Use the model to detect objects in the image.
## Implementation 
	Apply background subtraction to obtain the foreground mask.
	Use the mask to identify moving objects.
	Apply object detection to locate the objects.
   Classify the detected objects based on the trained model.

	Apply background subtraction to obtain the foreground mask.
	Use the mask to identify moving objects.
	Apply object detection to locate the objects.
   Classify the detected objects based on the trained model.

