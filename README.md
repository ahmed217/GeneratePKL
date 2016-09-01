# This notebook shows how to generate dataset from images for python (pkl file).

How to start: 

You create a folder (for example 'datafolder') and keep all your sample images in  the subfolder of that root folder. The names of the subfolder will be the class labels marked with numbers from 0 to number of folders. If you have 5 subfolders, then labels will be 0 to 4. The numbers are assigned to the subfolder names in the lexicographical order. 

At the top of the script, you can modify the variables according to your dataset. For example 'totaldata' should be equal to the number of total images. Next three variables training, validation, testcnt should be modified as your need; how many example you want for training (you can put the percentage or you can put exact number)

The next comes the tuple of image size. (height, width, channel) - this should be your target image size. The channel is GRAY or RGB. For GRAY it is 1, RGB it is 3. 
 
