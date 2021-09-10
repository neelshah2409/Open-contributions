## Image Segmentation
Image Segmentation is the process by which a digital image is partitioned into various subgroups (of pixels) called Image Objects, which can reduce the complexity of the image, and thus analyzing the image becomes simpler.

**Image segmentation Techniques**
we have the following techniques for image segmentation.
- Threshold Method
- Edge Based Segmentation
- Region Based Segmentation
- Clustering Based Segmentation
- Watershed Based Method
- Artificial Neural Network Based Segmentation

## Contour
 **How Contour Detection Works**
 At a high level, here is the 5-step process for contour detection in OpenCV:

 - 1> Read a color image
- 2>Convert the image to grayscale
- 3>Convert the image to binary (i.e. black and white only) using Otsu’s method or a fixed threshold that you choose.
- 4>If the objects in the image are black, and the background is white, we need to invert the image so that white pixels become black and black pixels become white. 
- 5>Detect the contours

## Feature Detection
Lets understand it with the help of example.
-![Image](https://opencv24-python-tutorials.readthedocs.io/en/stable/_images/feature_building.jpg)
- A and B are flat surfaces, and they are spread in a lot of area. It is difficult to find the exact location of these patches.

- C and D are much more simpler. They are edges of the building. You can find an approximate location, but exact location is still difficult. It is because, along the edge, it is same everywhere. Normal to the edge, it is different. So edge is much more better feature compared to flat area, but not good enough (It is good in jigsaw puzzle for comparing continuity of edges).

- Finally, E and F are some corners of the building. And they can be easily found out. Because at corners, wherever you move this patch, it will look different. So they can be considered as a good feature. So now we move into more simpler (and widely used image) for better understanding.

## Blending and Pasting Images

- The image pasting is a process of overlaying one image on top of the other. To successfully apply this process in OpenCV we need to select Region of Interest (ROI) in the first image, and then apply masking and some logical operations to overlay second image over the first image.
- The process of blending s done through the cv2.addWeighted() function from OpenCV. This function uses both the input images, assigns certain weights to each image pixel, adds them together and outputs the result into a new pixel. In that way we will get the us an impression of transparency. In the following example you can see the difference between pasting one image on top of other and blending two images together.
- ![Image](http://media5.datahacker.rs/2020/12/119-1024x409.jpg)

## Blurring Image 

- When processing an image, we are often interested in identifying objects represented within it so that we can perform some further analysis of these objects e.g. by counting them, measuring their sizes, etc. An important concept associated with the identification of objects in an image is that of edges: the lines that represent a transition from one group of similar pixels in the image to another different group. One example of an edge is the pixels that represent the boundaries of an object in an image, where the background of the image ends and the object begins.

- When we blur an image, we make the color transition from one side of an edge in the image to another smooth rather than sudden. The effect is to average out rapid changes in pixel intensity. The blur, or smoothing, of an image removes “outlier” pixels that may be noise in the image. Blurring is an example of applying a low-pass filter to an image. In computer vision, the term “low-pass filter” applies to removing noise from an image while leaving the majority of the image intact. A blur is a very common operation we need to perform before other tasks such as edge detection. There are several different blurring functions in the skimage.filters module, but the main one is the Gaussian blur.

## Face Detection
Steps for face detection
- Face Detection: The very first task we perform is detecting faces in the image or video stream. Now that we know the exact location/coordinates of face, we extract this face for further processing ahead.
- Feature Extraction: Now that we have cropped the face out of the image, we extract features from it. Here we are going to use face embeddings to extract the features out of the face. A neural network takes an image of the person’s face as input and outputs a vector which represents the most important features of a face.
- Saving the  image features.
- Comparing faces: Now that we have face embeddings for every face in our data saved in a file, the next step is to recognise a new t image that is not in our data. So the first step is to compute the face embedding for the image using the same network we used above and then compare this embedding with the rest of the embeddings we have


#### Neel Shah
mail-id : shahneel2409@gmail.com
