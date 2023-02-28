# Make the robot see
**List the names and NetID for your partners here.**

Alan Hsieh - amh425@cornell.edu

Cealia Pai - yp332@cornell.edu


Continue Lab 3 from last week. This week's material can be done rather quickly.


## Prep

### For this lab, you will need:
1. Your laptop

### Before you come to the lab on Thursday, please do the following:
1. install vnc viewer from [here](https://www.realvnc.com/en/connect/download/viewer/) if you haven't. 

### Deliverables for this lab are: 

0. A screenshot of the working VNC viewer with a working image view.

1. Answers to the reflection questions in part D. 

### The Report 
This README.md page in your own repository should be edited to include the work you have done (the deliverables mentioned above). Following the format below, you can delete everything but the headers and the sections between the **stars**. Write the answers to the questions under the starred sentences. Include any material that explains what you did in this lab hub folder, and link it in your README.md for the lab.

## Lab Overview
For this assignment, you are going to:

A) [Connect your camera](#-a-connect-your-camera)

B) [Connect to your Pi (VNC Viewer)](#part-b-connect-to-your-pi-through-vnc-viewer)

C) [People Detection](#part-c-people-detection)

Labs are due on Tuesdays before class. Make sure this page is linked to on your main class hub page.

## Part A. Connect your camera
Plug in the Pi camera to your RPi.

## Part B. Connect to your Pi through VNC Viewer
Start VNC Viewer, if prompted to sign in, "select Use VNC without signing in" in the bottom.

In the text box "Enter a VNC Server address or search", type in `Your_RPi_IP:1` (e.g. `10.56.131.31:1`).
> When prompted "server not encrypted", click "continue"
<img src="Images/vnc_warning.jpg" width="300">

**Password**: `student`

You should now log in to your Pi through VNC Viewer.

> <img src="Images/vnc.jpg" width="300">

Open a terminal, install `libcamera-dev`.

```bash
sudo apt install libcamera-dev
```
> <img src="Images/terminal.jpg" width="300">

## Part C. People Detection
First, let's test if your camera is working properly. 
```bash
# In a terminal in VNC Viewer
cd
curl -LJO https://raw.githubusercontent.com/FAR-Lab/Mobile_HRI_Lab_Hub/main/Lab4/test_camera.py
python3 test_camera.py
```
**Please include a screenshot of the working VNC viewer with a working image view.**

This exercise is based on this [The Data Frog Tutorial](https://thedatafrog.com/en/articles/human-detection-video/#:~:text=People%20detection,work%20well%20in%20other%20cases.) online. Your CPU will get toasty, so put on a **heat sink**. 

```
# In a terminal in VNC Viewer
curl -LJO https://raw.githubusercontent.com/FAR-Lab/Mobile_HRI_Lab_Hub/main/Lab4/people_detection.py
python3 people_detection.py
```

Optional: Another example you can try is from [PyTorch](https://pytorch.org/tutorials/intermediate/realtime_rpi.html) (installed already on your system). You will need to write a few lines of code to load the labels yourself. 

## Part D. Reflection

Reflect on the following questions:

1. For your favorite prototyped interaction that you have thought of so far, reflect upon how a camera connected to your Pi could be useful.

Camera can be used to capture images or videos of an environment and transmit the data to the Raspberry Pi for processing and analysis. This data can then be used for various purposes, such as detecting motion or objects in the environment, tracking movements, or providing real-time surveillance.

2. What issues do you foresee with this setup? 

There could be potential challenges related to image quality, lighting conditions, and camera placement. For instance, if the camera is not positioned correctly, it may not capture the desired information or may result in distorted images

3. How is the temperature? How is the speed? How is the connection?

It's essential to ensure that the camera and Raspberry Pi don't overheat, and that the connection between the two devices is stable and reliable.

4. How is the view? Would it capture what you might need to see for your prototyped interaction (in question 1)?

About the view captured by the camera, it's important to ensure that the camera's field of view captures the necessary information for the intended purpose of the prototyped interaction. Depending on the specific project's requirements, the camera may need to be positioned in a particular way or have specific settings adjusted to capture the desired view accurately.


Labs are due on Tuesdays before class. Make sure this page is linked to on your main class hub page.

### Again, deliverables for this lab are: 

0. A screenshot of the working VNC viewer with a working image view.

1. Answers to the reflection questions in part D. 

