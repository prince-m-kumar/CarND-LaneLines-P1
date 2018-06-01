# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report



---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

## Description
The pipeline consists on six steps represented by six different functions:

- **grayAction**: Grayscale transform using **cv2.cvtColor** method.
- **blurAction**: Applies a Gaussian Noise kernel to the provided image using **cv2.GaussianBlur** method.
- **cannyAction**: Applies the Canny transform to find edges on the image using **cv2.Canny** method.
- **maskAction**: Eliminate parts of the image that are not interesting in regards to the line detection 
- **houghAction**: Returns an image with hough lines drawn.
- **weighted_img**:  **houghAction** output merge with the original image to show line draw.

The output of image and video:

- [test_output_image](test_output_image)
- [test_output_video](test_output_video)


### 2. Identify potential shortcomings with your current pipeline

- line on video shaking a lot
- masked of image need improvement for video
- Some point taking outside due to the brightness of that point



### 3. Suggest possible improvements to your pipeline

- redesign and find better way to improve line draw
- provide masked area for better look
Another potential improvement could be to ...
