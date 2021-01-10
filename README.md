# programs
opencv
OpenCV imread() method loads an image from the specified file. 
If the image cannot be read (because of missing file, 
improper permissions, unsupported or invalid format) 
then this method returns an empty matrix.

Syntax: cv2.imread(path, flag)

Parameters:
path: A string representing the path of the image to be read.
flag: It specifies the way in which image should be read. 
      It’s default value is cv2.IMREAD_COLOR

Return Value: This method returns an image that is loaded 
              from the specified file.

Note: The image should be in the working directory or a 
      full path of image should be given.

All three types of flags are described below:

cv2.IMREAD_COLOR: 
    It specifies to load a color image. 
    Any transparency of image will be neglected. 
    It is the default flag. 
    Alternatively, we can pass integer value 1 for this flag.
cv2.IMREAD_GRAYSCALE: 
    It specifies to load an image in grayscale mode. 
    Alternatively, we can pass integer value 0 for this flag.
cv2.IMREAD_UNCHANGED: 
    It specifies to load an image as such including alpha channel.
    Alternatively, we can pass integer value -1 for this flag.
# Importing the OpenCV library 
import cv2 as cv
# Reading the image using imread() function 
scene = cv.imread('scene.jpg', 1) # cv2.IMREAD_COLOR
cv.imshow('scene', scene)
cv.waitKey(0)
cv.destroyAllWindows()

sceneG = cv.imread('scene.jpg', 0) # cv2.IMREAD_GRAYSCALE
cv.imshow('sceneGray', sceneG)
cv.waitKey(0)
cv.destroyAllWindows()

# image = cv.imread('road.jpg', -1) # cv2.IMREAD_UNCHANGED
flower = cv.imread('flower.jpg', 1) # cv2.IMREAD_COLOR
cv.imshow('flower', flower)
cv.waitKey(0)
cv.destroyAllWindows()

road = cv.imread('road.jpg') # cv2.IMREAD_COLOR
cv.imshow('road', road)
cv.waitKey(0)
cv.destroyAllWindows()

cv2.imshow() method is used to display an image in a window. 
The window automatically fits to the image size.
 Syntax: cv2.imshow(window_name, image)
 Parameters: 
window_name: A string representing the name of the window 
             in which image to be displayed. 
image: It is the image that is to be displayed.

cv2.waitKey() is a keyboard binding function. 
Its argument is the time in milliseconds

cv2.destroyAllWindows() simply destroys all the windows 
 we created. If you want to destroy any specific window, 
 use the function cv2.destroyWindow()
 
 Image properties include number of rows, columns, and channels; 
type of image data; number of pixels; etc
The shape of an image is accessed by image.shape. image = cv.imread('scene.jpg', 0) # cv2.IMREAD_COLOR
print( image.shape )

image = cv.imread('scene.jpg', 1) # cv2.IMREAD_COLOR
print( image.shape )
Total number of pixels is accessed by img.size:'''
print( image.size )

cv2.resize()
the size of the image can be specified mannually or you can spcify the scaling factor 
