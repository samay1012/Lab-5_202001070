# Lab-5_202001070

IT314 Lab 5

Student Name: Samay Deepak Ashar
Student ID: 202001070

Static Tool Used: Mypy (Python)
Git repository used - https://github.com/python/psf-salt.git

Using Mypy on Python files in this repository:

1. Python file used: conf.py in the docs folder of the github repository

Command Prompt Output:

Microsoft Windows [Version 10.0.19044.1826]
(c) Microsoft Corporation. All rights reserved.

C:\Users\student\psf-salt\docs>python -m mypy conf.py
Success: no issues found in 1 source file

C:\Users\student\psf-salt\docs>

![Capture1](https://user-images.githubusercontent.com/123536462/225280990-3d22a448-fcb5-4318-9bad-2125780d2450.PNG)

2. Python file used: salt.py in tasks folder of the github repository

Command Prompt Output:

Microsoft Windows [Version 10.0.19044.1826]
(c) Microsoft Corporation. All rights reserved.

C:\Users\student\psf-salt\tasks>python -m mypy salt.py
utils.py:6: error: Cannot find implementation or library stub for module named "fabric.api"
utils.py:6: error: Cannot find implementation or library stub for module named "fabric"
salt.py:5: error: Cannot find implementation or library stub for module named "invoke"
salt.py:5: note: See https://mypy.readthedocs.io/en/stable/running_mypy.html#missing-imports
salt.py:6: error: Cannot find implementation or library stub for module named "fabric.api"
salt.py:6: error: Cannot find implementation or library stub for module named "fabric"
salt.py:7: error: Cannot find implementation or library stub for module named "fabric.contrib.files"
salt.py:7: error: Cannot find implementation or library stub for module named "fabric.contrib"
__init__.py:3: error: Cannot find implementation or library stub for module named "invoke"
Found 8 errors in 3 files (checked 1 source file)

C:\Users\student\psf-salt\tasks>

![Capture](https://user-images.githubusercontent.com/123536462/225280206-f68fe5e0-13a3-4924-beac-d672f7c7dee1.PNG)

Explanation of Errors:
The errors are related to the fabric module. Mypy detected the errors because the fabric module hasn’t been installed in the computer and so the functions related to it cannot be accessed.

3. Python file used: utils.py in tasks folder of the github repository

Command Prompt Output:

Microsoft Windows [Version 10.0.19044.1826]
(c) Microsoft Corporation. All rights reserved.

C:\Users\student\psf-salt\tasks>python -m mypy utils.py
utils.py:6: error: Cannot find implementation or library stub for module named "fabric.api"
utils.py:6: note: See https://mypy.readthedocs.io/en/stable/running_mypy.html#missing-imports
utils.py:6: error: Cannot find implementation or library stub for module named "fabric"
salt.py:5: error: Cannot find implementation or library stub for module named "invoke"
salt.py:6: error: Cannot find implementation or library stub for module named "fabric.api"
salt.py:6: error: Cannot find implementation or library stub for module named "fabric"
salt.py:7: error: Cannot find implementation or library stub for module named "fabric.contrib.files"
salt.py:7: error: Cannot find implementation or library stub for module named "fabric.contrib"
__init__.py:3: error: Cannot find implementation or library stub for module named "invoke"
Found 8 errors in 3 files (checked 1 source file)

C:\Users\student\psf-salt\tasks>

![Capture2](https://user-images.githubusercontent.com/123536462/225281128-39be80e8-be05-4c92-85f8-9c4c5216e96f.PNG)

Explanation of Errors:
The errors are related to the fabric and invoke modules. Mypy detected the errors because the fabric and invoke modules weren’t installed in the computer and so the functions related to it cannot be accessed.

