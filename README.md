# Tiny Wudang

The project has been privately created to provide mechanics and features which aren't part of the UE5 topdown template.
<br/><br/>
<img src="https://github.com/user-attachments/assets/c8cd064b-d70e-4f13-a6b9-9dcce3e55856" width="360" height="360">


The features and how to use them:
<br/><br/>

- [Click-To-Move mouse navigation](Click-To-Walk-navigation)
<br/><br/>
- [Dynamic Camera Pan](Dynamic-Camera-Pan)
<br/><br/>
- [Dynamic Fading](Dynamic-Fading)
<br/><br/>
- [Fake Tilt-Shift Visuals](Fake-Tilt-Shift-Visual)
<br/><br/>

### Click-To-Walk navigation

<img src="https://github.com/user-attachments/assets/59356722-e9d2-49cc-b5d1-e5e7ca0f6bad" width="360" height="360">
<br/><br/>

For a simple and intuitive click-to-move navigation, at first we need to set the mouse cursor to stay visible (upper graph).
Next we need to capture the click location in the game world and convert its coordinates to world space coordinates. 
The result is set as an end point on the navmesh and fed into a Simple Move To instruction in order for the character to find its way.

<img src="https://github.com/user-attachments/assets/4b5c239d-6ade-4a77-90af-3bdc1a44d17d" width="640" height="350">


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
<br/><br/>

### Dynamic Fading

In order to be able to navigate inside roofed areas, the occluding objects are faded out and in via overlap events.

<img src="https://github.com/user-attachments/assets/6e90cfb3-3997-4c20-9c80-5f1319d02135" width="640" height="350">
<br/><br/>

In order to be able to edit the material at runtime, we need to create a dynamic material instance from the original roof material (upper graph).
Then we set up the entry and exit events for a collision box inside the house/ the area in which we want to trigger the fading effect. 
The fading follows a Timeline transition again and is simply reversed for the exit event.
<br/><br/>
<img src="https://github.com/user-attachments/assets/03499c74-a520-4ba5-a378-f0d5cedd03e6" width="640" height="350">
<br/><br/>

NOTE: all occluding objects' collision needs to be set to "NoCollison" in order to be able to click 'inside' without being blocked, also Create Overlap Events needs to be checked too:
<br/><br/>
<img src="https://github.com/user-attachments/assets/672de498-c33e-4ede-9eff-c1f01f82e450" width="640" height="350">


### Fake Tilt-Shift Visual

Here's the camera settings for the fake tilt-shift effect:
<br/><br/>
<img width="584" height="820" alt="image" src="https://github.com/user-attachments/assets/fa53078f-d523-427a-b091-58ec80564689" />



All assets used in the project are free to download and use. The environment, the buildings, shaders and materials are created by me and are free to steal. 
The foliage is from the Fab project [FantasyAssets Vol3 - Trees and Bushes](https://www.fab.com/listings/5336591a-de77-4815-ba72-bc4d130e5611), which is also free to download from tha Fab store.
<br/><br/>

<img src="https://github.com/user-attachments/assets/c0efc868-512c-4a02-831e-2473faa695a3" width="640" height="640">








