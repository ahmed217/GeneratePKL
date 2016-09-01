# This notebook shows how to generate dataset from images for python (pkl file).

##How to start: 

To create pkl file from the images, you need to create a folder (for example 'imagedata') and keep all your sample images in  the subfolders of that folder. The names of the subfolders will be the class labels marked with numbers from 0 to number of subfolders. If you have 5 subfolders, then labels will be 0 to 4. The numbers are assigned to the subfolder names in the lexicographical order. 

For example 
<pre>
./imagedata |
       | - pothole
       | - personbike
       | - construction
</pre>

In the above folder structure pohole, personbike, construction will be the labels sorted in lexicographical order ['construction','personbike','pothole']. The labels will be from 0 to 2 i.e., {'pothole': 2, 'personbike': 1, 'construction': 0}

At the top of the script, you can modify the variables according to your dataset. For example 'totaldata' should be equal to the number of total images. Next three variables training, validation, testcnt should be modified according to your need; how many examples you want for training (you can put the percentage or you can put exact number), how many examples for validation and how many for testing.

The next variable is the tuple of target image size. (height, width, channel) - this should be your target image size. The channel is GRAY or RGB. If the input images are GRAY then channel value should be 1, if input images are RGB then the channel value is 3. The source images will be resized to the target (height, width).  
 
