# RiggedInteractions
## VR Interaction System for Unity's XR Interaction Toolkit

### Installation:

- Install Unity's XR Plugin Management & Unity's XR Interaction Toolkit along with the XR Starter Assets from the package manager
- Create an empty object and add the XR Interaction Manager & Input Action Manager, assign the XRI Default Input Actions to the Input Action Manager
- Head to Samples -> XR Interaction Toolkit -> (version) ->  Starter Assets and click on each Preset and in the Inspector at the top click 'Add to (Preset)'
- Head up to Edit -> Project Settings -> Preset Manager and under Action Based Controller name XRI Default Right Controller 'right' and XRI Default Left Controller 'left'
- Import the RiggedInteractions.unitypackage to your project
- Set Layer 7 to be 'Right Physics Hand', Layer 8 to be 'Left Physics Hand', Layer 9 to be 'Display Hands'
- Edit -> Project Settings -> Physics disable collision on the collision matrix between (Right Physics Hand - Right Physics Hand) and (Left Physics Hand - Left Physics Hand)
- Edit -> Project Settings -> Time, set Fixed Timestep to 1/90
- Edit - Project Settings -> Physics set Default Max Angular Speed to 150
- Drag the Rigged Player v2 prefab into your scene
- Click Play and hope for the best!

### Usage: 

Rigged Player v2 - The core prefab that holds the player and hands
  Rigged Hand Grabber - overriding the XR Direct Interactor, handles disabling the hand collision on select
  
Rigged Grab Interactable - Put this onto any object you want to grab, some important settings: 
- Rigged Grab Type: 
  - Offset Grab - will use the hand's position as the grab point
  - Standard - the standard grab interactable usage, will snap to the attach point of the object
