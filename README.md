# Intro_to_Fiji_Basics

Tutorial and materials to follow along Introduction to Fiji workshop given by the ABIF in May 2020, covering basics of image processing and analysis in Fiji.

## Video tutorial

A recording of this workshop is available at [https://youtu.be/3Yfk9yjt3CA](https://youtu.be/3Yfk9yjt3CA)

[![ABIF-workshop: Introduction to Fiji - Basics](https://user-images.githubusercontent.com/64212264/142287396-4dad3326-63df-46c4-ba7a-58e2e98a3193.png)](https://youtu.be/3Yfk9yjt3CA)


<br />

The guidelines in the Objectives below below are purposefully vague to encourage you to find the commands in the menus of the main Fiji window. We encourage you to try to find these functions yourself, or follow along with the YouTube video. When in doubt, you can also use the search bar in the main Fiji window to find a command, and where it is located in the menus. 


In this repository you will find the images needed for today's interactive activity on image analysis.


<br />


Already familiar with the basics? Please check out our [introduction to writing macros in Fiji ](https://github.com/ABIF-McGill/Intro_to_Fiji_Macros)

<br />


## Download image data and Fiji

**To download the images** click on the green Code button, and then "Download ZIP". Then, you can extract images (ending in .tif) in Windows / OS X.

To download Fiji/ImageJ [click here](fiji.sc)



<br />



## Objective: Learn basics of opening images in Fiji, processing and object segmentation

The following is meant as a general guideline. We will discuss how to do this and why in class.

### Part 1) Loading an image in Fiji

In this section, we'll load an image in Fiji, and get familiarized with Fiji. We'll look at pixel intensity values and coordinates, adjust display contrast and LUTs.


### Part 2) Segment nuclei from an image of Hoechst stained nuclei and measure intensity

1) Open Fiji, then open the Hoechst image (“ESCs_WT_020_Ch2_Hoechst.tif") in Fiji by
dragging the file into the main window.

2) Duplicate the image.

3) Fluorescence images have a bit of noise, so try applying a Median Filter (with a radius of 1
pixel), to filter out some of that noise.

4) Since the staining has high variance, try applying a gaussian blur, to blur out the image a
little bit, to make thresholding easier.

5) Duplicate the gaussian blurred image from Step 4, then try to find a Threshold value which
will clearly delineate nuclei from background. Don’t worry if it’s not perfect - it never is!

6) If you have found a decent threshold value, try applying that threshold to generate a binary
image.

7) If the binary image has holes inside the nuclei, try to find a way to Fill Holes.

8) At this point, the measurements that will be made need to be set in Fiji. Open Set
Measurements, and select measurements which might be interesting, such as the area,
mean intensity, intensity standard deviation, etc.

9) On the binary image, try to create ROIs manually by using the Magic Wand Tool, like the
one in Photoshop, and press “T” to store the ROIs - alternatively, try to get Fiji to find all the
ROIs by using Analyze Particles. Once you have some Regions of Interest, open the U1-
GFP image (“ESCs_WT_020_Ch1_U1GFP.tif”), and use the ROIs that were created with the
Hoechst image to Measure U1-GFP intensity inside each nuclei. 


<br />

## Some notes

What seemed to work ok, and where were there problems with regards to segmenting
nuclei? Alternatively, how could the images be improved by adjusting the microscope image
acquisition parameters to make segmentation of nuclei easier?

<br />

Now you have the GFP intensities from some cells, which is great! What do these values mean?
How could they be compared? Is there a way to process many images, in cells from different
conditions, how could this be done to measure the intensity information and make a meaningful
plot?

<br />

Stuck? Don’t worry! If you are a bit lost, or searching desperately for a command, you’re
definitely not alone, and you have a few options!

<br />

First, on the main Fiji window, there is a little search field - here you can search for functions
that you think exist in Fiji, but that you can’t quite find in the menus. This search field is your
friend.

Then, if you are looking for something, but can’t quite distill it to a few keywords, go ahead and
google it. Chances are high someone else had your exact problem, and a community of Fiji
folks responded with helpful discussion and suggestions. For any analysis task, either in Fiji or
how to analyze the data, Google is your friend!


And of course, if you are doing this during an online webinar or tutorial, go ahead and ask a
question or put up your hand.

You’ll notice Fiji has a few idiosyncrasies with which one must get familiar. For example, we
duplicate our images regularly (when they aren’t too big), because Undo doesn’t work with
many functions, and often you need to try different settings to find what works for your images.
There are lots of odd little things like this in Fiji, don’t despair, you’ll get used to them pretty
quickly.


