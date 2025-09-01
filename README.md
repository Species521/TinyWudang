# Tiny Wudang

The project has been privately created to provide mechanics and features which aren't part of the UE5 topdown template.

The features and how to use them:

### Click-To-Walk navigation

<img src="https://github.com/user-attachments/assets/59356722-e9d2-49cc-b5d1-e5e7ca0f6bad" width="360" height="360">

### Dynamic Camera Pan

<img src="https://github.com/user-attachments/assets/0dcb78be-a192-4f00-81a1-7a6f8bda4312" width="640" height="350">
<br/><br/>

There are two collision boxes at the far end of the level, BP_camera_change_01 & 02.

<img src="https://github.com/user-attachments/assets/94037aff-accc-423d-8354-127baf7c5f43" width="640" height="350">
<br/><br/>

Their blueprint is set up as follows:

<img src="https://github.com/user-attachments/assets/b4abfcfb-792b-45f9-9e89-56470465291e" width=640 height="350">
<br/><br/>

The collision boxes register the entry and exit of overlaps and cast the camera angle re-adjustment instructions to the Custom Events in the character blueprint.
There they are picked up and the camera angle will change over time via a Timeline node upon entry and back upon exit.

<img src="https://github.com/user-attachments/assets/0ed401e9-90b0-44f0-97aa-4a8bbc8fe09a" width="350" height="350">


Custom Character


Fake Tilt-Shift Camera


All assets used in the project are free to steal. The environment, the buildings, shaders and materials are created by me and are free to steal. 
the foliage is from the Fab project "FantasyAssets Vol3 - Trees and Bushes", which is also free to download.


