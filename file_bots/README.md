Synopsis:

This module aims to assist with file-folder related chores.  I wish to only give minimal instructions to an assitant (e.g., a folder, and the features  of the filenames that I want to find), then the assitant will go and find those exact files, and do some simple organising tasks, like, 1) put the files in a new folder, 2) delete the files, 3) do something convenient about the files. 

The steps of using this module follow the line of thought above. Think of the module/class as a robot. To instantiate the bot, give it two initial pointers: 
a). The folder you want it to work on.
b). An exact description of the kind of files (search by filenames currently, but I may add more features later) you want to find (use regular experessions in python).

The bot can then do the following tasks. You only need to specify the task/method name:
M0. [the .locate method]: Locate and show the files. 

After M0, it will have 'a memory' of the files and do more, e.g.
M1. [the .copy_to_folder method] copy the files in M0 to another folder.

M2. [the .clean method] Clean up files in M0 by deleting them.

The bot currently specialises in pdf files, hence the suffix of \_pdf in its name. If the files in M0 are pdfs, bot can do two more things:
M3. [method .merge_pdf_tree] Merge pdfs in their subfolders and put them in the last leaf-folder where they are merged. An example is that you have 
30 books (folders), each folder contains 10 chapters (pdfs).  The bot will bind the chapters and produce
a merged pdf for each book and put them in their own folders. 

M4. [method .merge_pdf_all]  It can merge all located pdfs found in M0, no questions asked, period. I use M0 +  M4 regularly to merge pdfs. 


This folder contains:
README
file_bot_pdf.ipynb: Jupyter notebook explaining how to import the module and use the class/methods
file_bot_pdf.py: python code module

Tests:
Examples of how to import and test the code can be found in the Jupyter notebook.

Note:
The robot is likely to acquire other specialities as time goes by, so watch for version update! Or seriously, Siri should be able to do  this already (why hasn't it ?!). 

Bug report to: Dr Tiantian Yuan
www.linkedin.com/in/tiantianyuan                                                                     
