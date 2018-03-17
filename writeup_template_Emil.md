# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. 
1- I converted the images to grayscale
2- I applied Gussian Blure filter 
3- I applied Canny Edge detection
4- I determined the region of interest 
5- I applied hough line transform 
6 -I conslideated and extarplotation the line using the avergae of line data coordinates x1 ,y1, x2,y2 and the slope and also filtered out the outlier slopes
7- I draw the extraploated line over the images and videos


In order to draw a single line on the left and right lanes, I modified the draw_lines() function by:
line data coordiante points didvided into 2 cluser based on the sign of the slop one group with +ve slope and another group with -ve slope  to deffrenicate betweewn right and left line
I conslideated and extarplotation the line using the avergae of line data coordinates x1 ,y1, x2,y2 and the slope and also filtered out the outlier slopes



If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline

the pipeline is perfcetly working on all images and video except the optional question challenge clip one having some issuse in the tree shadow and low visiblity of the yellow lane





### 3. Suggest possible improvements to your pipeline

A possible improvement would be to for optional question challenge clip to add color maksing and darken the gray scale image to improve the hough lines


