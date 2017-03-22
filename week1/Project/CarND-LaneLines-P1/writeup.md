#**Finding Lane Lines on the Road** 

##Writeup Template

###You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

###1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale using the grayscale helper function, then I use the output of the grayscale function to apply a canny filter to detect edges. Once the edges are detected I do a polynomial fit to extract the vertices within the region of interest. Finally, I apply the hough line algorithm to detect lines. However, this algorithm in its original form doesnt draw a single line on the left and right lines. I then modified the draw_lines() functions to find the line equation and average out the slope values to draw a single line. 

#![alt text][image1]


###2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the image is too blurry. In that case, I think one could apply the bilateral filter as a preprocessing step. 


###3. Suggest possible improvements to your pipeline

A possible improvement would be to play with the parameters and tune it accordinlgy depending on the lightning conditions.

