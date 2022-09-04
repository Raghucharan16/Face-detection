# Face-detection using openCV

Face detection using Haar cascades is a machine learning based approach where a cascade function is trained with a set of input data. OpenCV already contains many pre-trained classifiers for face, eyes, smiles, etc.. Today we will be using the face classifier. You can experiment with other classifiers as well.

You need to download the trained classifier XML file (haarcascade_frontalface_default.xml), which is available in OpenCv’s GitHub repository. Save it to your working location.

A few things to note:

The detection works only on grayscale images. So it is important to convert the color image to grayscale.

detectMultiScale function is used to detect the faces. It takes 3 arguments — the input image, scaleFactor and minNeighbours. scaleFactor specifies how much the image size is reduced with each scale. minNeighbours specifies how many neighbors each candidate rectangle should have to retain it. You can read about it in detail here. You may have to change these values to get the best results.  [Refer the Code]

faces contains a list of coordinates for the rectangular regions where faces were found. We use these coordinates to draw the rectangles in our image.
