# How to generate pkl dataset from images for python.

##How to start: 

To create pkl file from the images, you need to create a folder (for example 'imagedata') and keep all your sample images in  the subfolders of that folder. The names of the subfolders will be the class labels marked with numbers from 0 to number of subfolders. If you have 5 subfolders, then labels will be 0 to 4. The numbers are assigned to the subfolder names in the lexicographical order. 

For example 
<pre>
./imagedata |
       | - pothole
       | - personbike
       | - construction
</pre>

In the above folder structure pohole, personbike, construction will be the labels sorted in lexicographical order 

```python
['construction','personbike','pothole']
```

The labels will be from 0 to 2 i.e., 

```python
{'pothole': 2, 'personbike': 1, 'construction': 0}
```

##Variables     
At the top of the script, you can modify the variables according to your dataset. For example 'totaldata' should be equal to the number of total images. Next three variables training, validation, testcnt should be modified according to your need; how many examples you want for training (you can put the percentage or you can put exact number), how many examples for validation and how many for testing.

The next variable is the tuple of target image size. (height, width, channel) - this should be your target image size. The channel is GRAY or RGB. If the input images are GRAY then channel value should be 1, if input images are RGB then the channel value is 3. The source images will be resized to the target (height, width).  

* **data** -- this is a numpy array which has rows equal to totaldata, and columns equal to (height * width * channel). Each row of the array stores a (height, width) images of given channel. The first entries contains the RED channel values, the next the GREEN, and the final entry the blue. The image is stored in row-major order, so that the first entries of the array are the red channel values of the first row of the image. 
* **labels** -- a list with numbers. The number at index *i* indicates the label of the *i*th image in the array **data**. 



