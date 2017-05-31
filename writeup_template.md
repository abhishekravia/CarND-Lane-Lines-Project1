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

First, I converted the images to grayscale, then I smoothened the image used gaussian blur function provided in the helper function. Next, I created a edge imageusing the canny edge detector to locate all the edges. Then I selected the region of interest so that I can focus on the important lane lines and not the other parts. This helped in eliminating the stray lines . Next is the created a hough image to fing the intersections at each point and hence find the lane lines..... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by calculating the slope between two points of x1,y1 nad x2,y2. Then I classify thenminto positive and negative slopes and keep adding them to an array and find the averages of each quantities to draw a line between the two points of min and max.

If you'd like to include images to show how the pipeline works, here is how to include an image: 


![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
