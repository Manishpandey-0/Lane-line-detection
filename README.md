<a name="br1"></a> 

Lane Detection

**Manish Pandey,**

**MTech, Data Science**

**2022pds0024@iitjammu.ac.in**



<a name="br2"></a> 

**Introduction**

1\.Lane Detection is a project that focuses on developing a system for accurate detection

and visualization of lane lines on roads.

2\.The project utilizes computer vision techniques and image processing algorithms to

identify lane lines in real-time from input images or videos.

3\.The primary goal of this project is to improve road safety by providing a visual

representation of detected lane lines, enabling autonomous vehicles to navigate within

lanes and make informed decisions.

4\.This project has significant applications in the field of autonomous driving systems,

where precise lane tracking is essential for ensuring safe and efficient navigation,

contributing to the advancement of autonomous vehicle technology.



<a name="br3"></a> 

Importance of Lane Detection in Autonomous

Driving Systems:

• Autonomous vehicles rely heavily on computer vision and sensor

technologies to perceive the environment and make informed

decisions.

• Lane detection enables autonomous vehicles to stay within

designated lanes.

• Accurate lane detection improves vehicle safety, reduces accidents,

and enhances overall driving experience.



<a name="br4"></a> 

Lane Detection Pipeline

1\.Gray Scale

2\.Gaussian Smoothing

3\.Canny Edge Detection

4\.Region Masking

5\.Hough Transform

6\.Draw Lines [Mark Lane Lines with different Color]



<a name="br5"></a> 

**Gray scaling**

• Processing of single channel is faster that three channel

processing.

0 to 355

0 to 255

3 channel

1 channel



<a name="br6"></a> 

Gaussian Smoothing

• Noise can be defined as unnecessary

information in a image or video.

• Reducing the noise with Gaussian filter by

modify the value of the pixels to the average

values of the pixels.

• Smooth out the image before applying

Canny edge detection so we do not detect

faint edges



<a name="br7"></a> 

• Edge detection refers to process of identifying and

locating sharp discontinuities in an Image.

**Edge**

**Detection**

• Different methods:

• Sobel Operator

• Laplacian of Gaussian filter

• Canny Edge Detection Algorithm

• Why Canny edge detection is more optimal?

• Less sensitive to noise

• It removes streaking by using two thresholds high

and low

• Offers good localization of edges and utilizes

gradient of the edge to generate thin edges



<a name="br8"></a> 

**Canny Edge Detection**

**Algorithm:**

• Smooth image with 2D gaussian :

• Compute image gradient with sobel operator:

• Find gradient magnitude at each pixel:

• Find gradient orientation at each pixel:

• Compute Laplacian along the gradient direction at each pixel:

• Find zero crossings in Laplacian to find the edge location



<a name="br9"></a> 

Canny edge

detection

results



<a name="br10"></a> 

Region Masking

• We want to narrow down our analysis to a section of the image. We use

masking for this purpose.

• We start by creating a blank mask with the same shape as the input

image.

• Create a polygonal mask over the vertices.

• Apply the polygonal mask to the original image resulting in a masked

image over the region of interest.



<a name="br11"></a> 

**Masking**

**Process**



<a name="br12"></a> 

Difficulties for fitting approach

• Extraneous data : Which points to fit to?

• Incomplete data : Only parts of the image

is

visible

• Noise

**Solution: Hough Transform**



<a name="br13"></a> 

Hough Transform: Concept



<a name="br14"></a> 

Multiple Line detection



<a name="br15"></a> 

Better Parameterization

• Issue:

• Slope of the line could be very large or very small

• More memory and computation

• Solution:

• Use

• Orientation of θ is finite ,i.e. it is between 0<sup>o</sup> and 180<sup>0</sup>

• Distance ρ is finite.



<a name="br16"></a> 

Better

Parameterization



<a name="br17"></a> 

• We perform Hough Transform to detect line (lane) from a

video

Hough Transform



<a name="br18"></a> 

Pipeline Outputs

Gray scaling



<a name="br19"></a> 

Pipeline Outputs

Gaussian Smoothing



<a name="br20"></a> 

Pipeline Outputs

Canny Edge Detection



<a name="br21"></a> 

Pipeline Outputs

Region Masking



<a name="br22"></a> 

Pipeline Outputs

Hough Transform



<a name="br23"></a> 

Final Output



<a name="br24"></a> 

Input

video



<a name="br25"></a> 

Output

video



<a name="br26"></a> 

Thank You!

