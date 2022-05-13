# Lesson: Interaction Design

### First and Last Name: Anastasia Kourfalidou

### University Registration Number: dpsd19060

### GitHub Personal Profile: AnastasiaKourfalidou

### Augmented Reality Personal Repository: https://github.com/AnastasiaKourfalidou/Augmented-Reality

# Introduction

In this project has been developed an example of an Interactive Web-based Augmented Reality Application, using the AR.js augmented reality library and the Α-Frame virtual reality library.

# Summary

In the first deliverable that has been developed so far, the Augmented Reality Application uses the camera and recognizes a default marker, named hiro. When the webcam finds and recognizes the hiro marker it displays a box, a cylinder and a sphere. In parallel, there is snow falling in the scene, which can be activated and deactivated using the speech commands start/stop accordingly.

# 1st Deliverable

For the development of the first deliverable the following features were implemented in index.html file:

1. It is added and displayed a cylinder and a sphere object in our scene. This has been done by adding the following lines of code after the default box object.

- <a-entity id="cylinder" geometry="primitive: cylinder; radius: 0.1; height: 1.0" position="-0.5 0 0" material="color: #FF66B2"></a-entity>
- <a-entity id="sphere" geometry="primitive: sphere; radius: 0.1; height: 1.0" position="0.5 0 0" material="color: #FFFF99"></a-entity>
  There are also adjustments at the dimensions of the objects as well as their color.

2.  There has been also added snow at the scene where the geometry objects are displayed, by using the Α-Frame particle system component. This was accomplished by modifying the source code by adding the following command:

- <a-entity id="snow" position="0 2.25 -15" particle-system="preset: snow; particleCount: 5000; size: 5"
  There are adjustments at the size of the particles and the particleCount variable which defines the total number of particles this emitter will hold.

3. Finally by using the Α-Frame speech command component we modified the source code, so when we give the speech command: stop it stops snowing, while when we give the speech command: start it starts snowing. In order to be able to use the speech recognition the following command had to be added fisrt:

- <a-entity id="annyang" annyang-speech-recognition></a-entity>

After that it was necessary to define the speech commands as it is shown:

- speech-command\_\_start="command: start; type: attribute; attribute: visible; value: true;"
- speech-command\_\_stop="command: stop; type: attribute; attribute: visible; value: false;">

They were added inside the snow entity because the functionality of the commands is referred to the snow. So when saying start it starts snowing and when saying stop it stops. Finally the code that was added looks like that:

- <a-entity id="snow" position="0 2.25 -15" particle-system="preset: snow; particleCount: 5000; size: 5"
   speech-command__start="command: start; type: attribute; attribute: visible; value: true;" 
   speech-command__stop="command: stop; type: attribute; attribute: visible; value: false;">
  </a-entity>

# Notes

The hiro image that was used for the testing of the application can be found here: https://stemkoski.github.io/AR-Examples/markers/hiro.png?fbclid=IwAR3Et4BlytI8UCNxuBxGnC29b8HIQFoa66OrXM7UmYqgPPMdO3mK9_J4N7Q

# 2nd Deliverable

# 3rd Deliverable

# Conclusions

# Sources
