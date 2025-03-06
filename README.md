# EXP4 Gradient-Operator-IPMV
Edges are significant local changes of intensity in a digital image. An edge can be defined as a set of connected pixels that forms a boundary between two disjoint regions. There are three types of edges: 

Horizontal edges
Vertical edges
Diagonal edges
Edge Detection is a method of segmenting an image into regions of discontinuity. It is a widely used technique in digital image processing like 
 pattern recognition
image morphology
feature extraction
Edge detection allows users to observe the features of an image for a significant change in the gray level. This texture indicating the end of one region in the image and the beginning of another. It reduces the amount of data in an image and preserves the structural properties of an image. 

EXP 4a 
This program processes an image to detect edges using the Sobel operator and visualizes the results. It begins by loading the image in grayscale, which simplifies the processing by reducing the image to a single intensity channel. The code checks whether the image is loaded successfully, and if not, it exits the program. The Sobel operator is then applied to compute the gradients of the image in both the x (horizontal) and y (vertical) directions. These gradients represent the rate of change in pixel intensity along each direction, which is crucial for edge detection. The Sobel function in OpenCV (cv2.Sobel) uses a kernel of size 3 to calculate the gradients. The program combines the x and y gradients to calculate the magnitude of the gradient at each pixel using cv2.magnitude. This magnitude highlights areas of significant intensity change, which are indicative of edges in the image. The result is then converted to an unsigned 8-bit integer format for proper visualization. Finally, the program uses Matplotlib to display three images side by side: the original grayscale image, the gradient in the x-direction, and the computed gradient magnitude, which emphasizes the edges. This process is commonly used in computer vision tasks such as edge detection for object recognition.

EXP 4b Roberts
This code applies the Roberts Cross operator to detect edges in a grayscale image. The image is loaded using OpenCV, and two 2x2 kernels (kernel_x and kernel_y) are defined for edge detection in the x and y directions, respectively. The cv2.filter2D function is used to convolve the image with these kernels to compute the gradients in both directions. The magnitude of the gradient is then calculated using the Pythagorean theorem. Finally, the original image, gradient in the x-direction, and gradient magnitude are displayed side by side using Matplotlib to visualize the edges detected by the Roberts operator.
