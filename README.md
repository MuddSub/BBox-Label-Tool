BBox-Label-Tool
===============

**New Update**
BBox-Label_Tool Adapoted from https://github.com/puzzledqs/BBox-Label-Tool

-Modified to be compatiable with python3

Convert.py adapted from https://github.com/Guanghan/darknet/blob/master/scripts/convert.py

-TODO: Modified to work with BBox-Label-Tool file system

Brief Instruction: the files inside the image folder are labeled by their class labels. For instance, you might label cat as class 001. Then to label cat, you want to move all images of cats to class 001 folder inside the image folder. Your labels should be generated insie the label folder. These labels are NOT in yolo's accepted format. To convert, use the convertion.py.

----------------

**Original README** 
Below is the original README for BBox-Label-Tool:

A simple tool for labeling object bounding boxes in images, implemented with Python Tkinter.

**Updates:**
- 2017.5.21 Check out the ```multi-class``` branch for a multi-class version implemented by @jxgu1016

**Screenshot:**
![Label Tool](./screenshot.png)

Data Organization
-----------------
LabelTool  
|  
|--main.py   *# source code for the tool*  
|  
|--Images/   *# direcotry containing the images to be labeled*  
|  
|--Labels/   *# direcotry for the labeling results*  
|  
|--Examples/  *# direcotry for the example bboxes*  

Environment
----------
- python 2.7
- python PIL (Pillow)

Run
-------
$ python main.py

Usage
-----
0. The current tool requires that **the images to be labeled reside in /Images/001, /Images/002, etc. You will need to modify the code if you want to label images elsewhere**.
1. Input a folder number (e.g, 1, 2, 5...), and click `Load`. The images in the folder, along with a few example results will be loaded.
2. To create a new bounding box, left-click to select the first vertex. Moving the mouse to draw a rectangle, and left-click again to select the second vertex.
  - To cancel the bounding box while drawing, just press `<Esc>`.
  - To delete a existing bounding box, select it from the listbox, and click `Delete`.
  - To delete all existing bounding boxes in the image, simply click `ClearAll`.
3. After finishing one image, click `Next` to advance. Likewise, click `Prev` to reverse. Or, input an image id and click `Go` to navigate to the speficied image.
  - Be sure to click `Next` after finishing a image, or the result won't be saved. 
