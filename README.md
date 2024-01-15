## Integrated Gradients Exercise/Demonstration
 
Integradient gradients are a way to try to understand what part of an input to an ML/AI model led to its classification.  More specifically, the data of interest is compared to a "baseline" input to see what in the input (relative to the baseline) results in the inputs classification. In the general case, the baseline should be "neutral" (e.g. *P(baseline)=50%*).  In the demonstration exercise here, the data of interest is an image of a digit 9, for an image digit classifier which classifies images of the digits 0,1,..., and 9. as zero, one, ..., or 9.  The baseline is a 4 (drawn with "open top style").  It makes some sense that the critical part of the image is what is in the top or upper-left and how the open-top is a distinguishing characteristic that can be used to distinguish a digit as being 9 or 4.

This repo containts some integrated gradients exdercises.

To run the exercises here, docker and Linux are required.

1.  Build the docker with a command like:
```
docker build . -t digit_ig_exercise
```
2.  Assuming the build is successful, start the container with a command like the one below:

```
docker run  -v ${PWD}:/tf/work  --rm -it -p 8888:8888 digit_ig_exercise
```
3.  Once the container starts, look for the URL.  Copy/past that into a new browser tab (being sure to include the password).  Next, navigate into the "work" directory and open the "keras_example.ipynb" file.  Run the cells, read the text or both!

