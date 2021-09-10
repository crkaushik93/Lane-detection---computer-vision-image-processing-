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

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]

Ans: In order to draw a single line on the left and right lanes, we introduced a function called as find_lanes and called the function in draw_lanes(). Here we have seperated the line segment on terms of left_lines and right_lines using the slope values derived from the slope equation as we know to decied which line belongs to left and right. Also, we averaged the position of the each lines to extrapolated to top and bottom such that they all belong one line segment in terms of left and right sides.

### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...

Ans: Shortcoming would be faced when the lines are hit by shadows or when the lines are hidden by cars or other menas of transportation that comes in contact or close to this car thus hidding the features to be extracted.Also, when identifying the lines there are cahnces that these lines are thrown out of interest caused due to change of lanes by the car as in this video we have discussed the feature extraction with respect to straight lines.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...

Ans: The possible changes or improvements that can be done in such shortcomings would be using the HSV color space when we have to deal with shadows or lanes that are hidden with respect to other cars.

Also, while extracting lanes when changes, machine learning algorithms could be useful in way of training the models about the extracted features.
