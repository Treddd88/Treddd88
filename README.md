# Computer Vision Techniques Using  Classified Systems 

Utilizing  fundamental techniques to detect moving objects in a background subtraction. 

For this implementation, I installed OpenCV and NumPy. 
The mask was used to identify moving objects. Detection was most useful to locate the objects. An algorithm will not be accurate, especially in environments with rapid changes. Therefore, objects detecting objects were difficult. A dataset with images of the three object types (cars, bicycles, pedestrians) was used to annotate.
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
   Classify the detected objects based on trained model.

## Code Reference 
<opencv_storage>
<cascade type_id="opencv-cascade-classifier"><stageType>BOOST</stageType>
  <featureType>HAAR</featureType>
  haar_cascade = 'cars.xml'
video = 'video.avi'      
cap = cv2.VideoCapture(video) 
car_cascade = cv2.CascadeClassifier(haar_cascade)
    # reads frames from a video 
ret, frames = cap.read() 
        
# convert frames to gray scale  
gray = cv2.cvtColor(frames, cv2.COLOR_BGR2GRAY) 
        
# Detects cars of different sizes in the input image 
cars = car_cascade.detectMultiScale
  <internalNodes>  
      (gray, 1.1, 1)
          <leafValues>
            cv2.rectangle(frames(0,0,255),2)</leafValues></_>
        <_>
          <internalNodes>
           # Display frames in a window 
              cv2.imshow('video', frames)</internalNodes>
          <leafValues>
        # loop runs if capturing has been initialized. 
while True: 
    # reads frames from a video 
    ret, frames = cap.read() 
        
    # convert to gray scale of each frames 
    gray = cv2.cvtColor(frames, cv2.COLOR_BGR2GRAY) 
        
    
    # Detects cars of different sizes in the input image 
    cars = car_cascade.detectMultiScale(gray, 1.1, 1) 
        
    # To draw a rectangle in each cars 
    for (x,y,w,h) in cars: 
        cv2.rectangle(frames,(x,y),(x+w,y+h),(0,0,255),2) 
    
    # Display frames in a window  
    cv2.imshow('video', frames) 
        
    # Wait for Esc key to stop 
    if cv2.waitKey(33) == 27: 
        break
    
# De-allocate any associated memory usage 
cv2.destroyAllWindows()</leafValues></_>
            
</opencv_storage>

	
