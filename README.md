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

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I applied gaussian blur after with i performed canny edge detection. I then chose region of interest (defined by the vertices of a polygon )and finally applied hough transformation.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...finding slopes of each line to classify them into left and right lanes. I took the average slope and intercept for each segment(left and right) and then used the average values to extrapolate the left and right lanes.

If you'd like to include images to show how the pipeline works, here is how to include an image: 


![solidwhitecurve](https://cloud.githubusercontent.com/assets/15799394/26694711/fdeb14de-4725-11e7-908d-40b413ab121c.jpg)
![solidwhiteright](https://cloud.githubusercontent.com/assets/15799394/26694712/ffd88e02-4725-11e7-8c6d-9ad0a28919c9.jpg)
![solidyellowcurve](https://cloud.githubusercontent.com/assets/15799394/26694714/026d12c8-4726-11e7-9d2c-64f21e63b3e4.jpg)
![solidyellowleft](https://cloud.githubusercontent.com/assets/15799394/26694720/08d8aec4-4726-11e7-8d75-d43f69b7f524.jpg)
![whitecarlaneswitch](https://cloud.githubusercontent.com/assets/15799394/26694728/0c2a73d2-4726-11e7-80cd-9c425aaa4881.jpg)


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be ...during curves the left/right lanes are moving over to the road

Another shortcoming could be ...region masking is fixed by co-ordinates, hence not working during bends


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...improve lane detections in the draw lanes function...so it will work for curves

Another potential improvement could be to ...improve region masking
