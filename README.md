# **Finding Lane Lines on the Road** 

When we drive, we use our eyes to decide where to go. The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle. Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.
In this project I detect lane lines in images using Python and OpenCV. OpenCV means "Open-Source Computer Vision", which is a package that has many useful tools for analyzing images.

### Reflection

### 1. My pipeline:

My image processing pipeline consisted of 5 steps:
1)  First, I converted the images to grayscale
2) I used canny detection to get the lines of the road.
3) I selected the region of the image that I wanted to analyze, using an image mask.
4) I run a Hough transform on the edge detected image.
5) I drew the lines on the edge image.

![](http://i.imgur.com/cFD9uTF.jpg)

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by finding the slop of each lane and then drew the lanes from the upper point to the lowest point.

### 2. Potential shortcomings with my current pipeline:

One potential shortcoming would be what would happen when the light conditions aren't great or it's night time. 
The lines might not be visible.
Another shortcoming could be if the car moves really fast, and we won't be able to process the images fast enough. 

### 3. Possible improvements:

A possible improvement would be to use more technics to anyalize the position of the lane lines.
Another potential improvement could be to use a pre existing data about the road.

Videos showing the result :

[![Yellow](http://i.imgur.com/VZ0V5F7.png)](https://vimeo.com/229834462 "Yellow")

[![White](http://i.imgur.com/NslDAD3.png)](https://vimeo.com/229834451 "White")
