# 👁️ Week 2: Learning to See — Manipulating and Understanding Images  
**Working with Filters, Color Spaces, Histograms, and Drawing on Frames**

---

## 🧪 What You’ll Learn This Week

- Image filtering and convolution  
- Blurring, sharpening, and edge detection  
- Understanding color spaces: RGB, HSV, Grayscale  
- Histogram analysis and equalization  
- Accessing live video feed from a webcam  
- Drawing shapes and adding text to frames  
- Introduction to real-time object detection using Ultralytics YOLO  

---

## 🎥 Accessing the Webcam

Learn how to open your computer’s webcam using OpenCV and display the live video feed. You’ll also learn how to manipulate that feed in real time.

📺 **Watch**: [Accessing Webcam in OpenCV](https://youtu.be/FygLqV15TxQ?feature=shared)

```python
import cv2

cap = cv2.VideoCapture(0)

while True:
    ret, frame = cap.read()
    if not ret:
        break
    cv2.imshow("Webcam", frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
```

---

## 🔲 Drawing Shapes & Adding Text

Learn how to overlay rectangles, circles, lines, and text on video frames or images—an essential step for visualizing results (like detections).

📺 **Watch**: [Draw Rectangle on Video](https://youtu.be/UcRmCehhQUM?feature=shared)  
📘 **Read**: [Drawing Shapes and Text - Tutorialspoint](https://www.tutorialspoint.com/opencv_python/opencv_python_drawshapes_text.htm)

---

## 🧠 What is Image Filtering (Convolution)?
In image processing, convolution is the process of applying a filter or kernel to an image to transform it. A kernel is a small matrix that is slid across the image, performing mathematical operations on the pixel values.

Common convolution operations include:

Blurring: Removes noise and details by averaging surrounding pixels.

Sharpening: Highlights edges and details by subtracting a blurred version.

Edge Detection: Highlights transitions using kernels like Sobel, Laplacian, or Canny.

📖 Read:

[A Gentle Introduction to Image Convolution](https://towardsdatascience.com/image-convolution-how-filtering-works-37a950e7784d)

- **Blurring**: Remove noise  
- **Sharpening**: Highlight edges  
- **Edge Detection**: Detect objects' outlines  

🔧 Key Functions:

```python
cv2.GaussianBlur(), cv2.medianBlur(), cv2.Canny(), cv2.Sobel()
```

📘 _Practice Tip:_ Use different kernels and observe how they affect the image.

---

## 🎨 Understanding Color Spaces

Images are stored as arrays of pixels with color information. Different color spaces allow for better manipulation depending on your task.

RGB (Red, Green, Blue) – Most common format, used for display.

Grayscale – Reduces an image to one channel, useful for edge detection or thresholding.

HSV (Hue, Saturation, Value) – Great for isolating color-based features.

Real-world use:

Detecting ripe fruit? HSV is better than RGB for color segmentation.

Face recognition? Convert to grayscale first to simplify the input.

📖 Read:

[Color Spaces in Computer Vision](https://learnopencv.com/color-spaces-in-opencv-cpp-python/)

[Why HSV is better than RGB for color detection](https://stackoverflow.com/questions/20792445/calculate-rgb-value-for-a-range-of-values-to-create-heat-map)


Switch between RGB, Grayscale, and HSV to work with color more effectively.

```python
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
```

👁️ Use HSV masks to detect specific colors in an image or video stream.

---

## 📊 Histograms & Equalization

 - A histogram plots how frequently each pixel intensity occurs. It helps you:

 - Detect low contrast (narrow peaks)

 - Decide thresholds for binarization

Perform Histogram Equalization to improve image clarity

📖 Read:

[Image Histograms in OpenCV](https://docs.opencv.org/4.x/d1/db7/tutorial_py_histogram_begins.html)

[What is Histogram Equalization?](https://en.wikipedia.org/wiki/Histogram_equalization)

```python
equalized = cv2.equalizeHist(gray)
```

Use `matplotlib` to plot histograms and visualize changes.

---

## 🧠 Bonus: Object Detection with YOLO (Ultralytics)

YOLO (You Only Look Once) is a real-time object detection algorithm that divides images into grids and predicts bounding boxes and class probabilities.

It’s widely used in:

Surveillance cameras

Autonomous vehicles

Retail analytics

Waste segregation (Sustainability applications!)

📖 Read:

[YOLOv8 Docs by Ultralytics](https://docs.ultralytics.com/)

[YOLO Explained in Simple Terms](https://blog.roboflow.com/yolov8-guide/)

Begin your journey into real-time object detection using **Ultralytics YOLOv8**.

📘 **GitHub**: [Ultralytics YOLO GitHub Repo](https://github.com/ultralytics/ultralytics)  
📺 **Watch**: [Object Detection on Images using YOLOv8](https://youtu.be/65eK8ZoY1p4?feature=shared)

💡 Install Ultralytics:
```bash
pip install ultralytics
```

Run detection on an image:
```python
from ultralytics import YOLO

model = YOLO("yolov8n.pt")
results = model("your_image.jpg", show=True)
```

---

## 📁 This Week's Practice Tasks

- Open webcam and draw rectangle around faces  
- Draw text labels on moving video feed  
- Convert webcam stream to grayscale and display both original and grayscale  
- Plot image histogram and equalize contrast  
- Perform basic object detection using Ultralytics YOLO  

---

## 📝 Your Takeaways by Week’s End

✔️ Use OpenCV to access webcam and process live video  
✔️ Add overlays to images and videos (shapes, labels)  
✔️ Manipulate color channels and convert between spaces  
✔️ Enhance and analyze image contrast using histograms  
✔️ Run a simple YOLOv8 object detector on images  


### 💬 Questions to Reflect On:

> Why might you convert an image to grayscale before processing it?
>
> What are the tradeoffs between Sobel and Canny edge detection?
>
> What kind of image issues can histogram equalization fix?
>
> Why is HSV more robust than RGB for detecting colored objects under varying lighting?
>
> How does a kernel’s size affect the outcome of a convolution operation?
