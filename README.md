# EnfluxUnitySDK
This is the Enflux Unity SDK with support for VR, animation recording, and playback.

**The documentation and tutorial is updated, so check back frequently.**

&nbsp;
## Unity SDK
------
* Our SDK is built for Unity 5.4.0f3 and newer.
* Check [releases tab](https://github.com/Enflux/EnfluxSuitController/releases)

&nbsp;
## Instructions For Setup
------
1. Download Enflux Unity SDK.
2. Start or open a Unity project.
3. Under the <i>Assets</i> tab select <i>Import Package > Custom Package</i>.
4. Navigate to folder containing `Enflux.unitypackage` and select package.
5. A window will open, select "Import".
6. Under Project tab, expand <i>Enflux > SDK > Prefabs</i>
7. Drag and drop the following into Hierarchy:
  * `[EnfluxManager]`
  * `[EnfluxHumanoid]`
8. If one is not already in the project, add a `Canvas`.
  * From <i>Enflux > SDK > Prefabs > UI</i>, drag `[EnfluxExampleConnectionPanel]` onto a `Canvas`.
9. Move camera and `[EnfluxExampleConnectionPanel]` as needed.

&nbsp;
## Instructions For Setup With VR
------
### HTC Vive Requirements
1. Obtain and import [SteamVR Unity SDK](https://www.assetstore.unity3d.com/en/#!/content/32647)

### Oculus Rift Requirements
1. Obtain and import [Oculus Unity SDK](https://developer3.oculus.com/downloads/)

### VR Setup
1. Replace the `[EnfluxHumanoid]` prefab with `[EnfluxVRHumanoid]` prefab.
2. In the `HMD Adapter` component, drag the main camera to the field `HMD`.
3. The humanoid will now follow the camera, where the head is placed at the camera location.
4. Lower the camera's near clipping plane close to zero.
4. In <i>Edit > Project Settings > Player</i> make sure "Virtual Reality Supported" is on.

&nbsp;
## Connection Instructions And Issues
------
1. Turn on the Enflux modules you plan to use. In Windows Bluetooth Manager, click "Pair" on all Enflux modules you wish to use.
2. Open the Unity project.
3. On an `EnfluxManager` component, there will be buttons to connect and calibrate the clothing.
![alt tag](https://lh6.googleusercontent.com/_Q0r-b9FlYv3qvsUrDYpqsuQ64z0cT5d7dbE1stujSbhqAVkHxo90Rp5WvmiYwPnwl_ipUHJAJG8fSw=w3440-h1310)
4. If this first time using the suit or in a different environment, click Calibrate first. This process will optimize the suit for the environment.
  * [Calibration Tutorial](https://youtu.be/HKrl9DVYESI)
6. After calibrating (if neccessary) and connecting, the module will initialize for around 2 seconds. **USER NEEDS TO BE STANDING STILL FOR MOST ACCURACY.**
6. After initiaization has completed, the suit should begin animating.
7. If the wants to start the suit facing another direction, face that direction, assume a straight posture, and click Reset Orientation.
8. When done using the suit, click Disconnect.

&nbsp;
* If the device is unable to connect and shows "Paired" in Windows Device Manager, it may have went to sleep to conserve battery. Try turning it back on.
* If the device is still unable to connect, unpair it in Windows. Hard reset by pressing the module button down for 3 seconds until the light turns solid blue, then re-pair.

### Troubleshooting Guide 
For common issues, check:
https://docs.google.com/document/d/1_1er5wxuVvz53wxTvzeSnaUbJ6NVyUM8AZqgQ3K6RxY

&nbsp;
## Example Scenes
------
* These can be found under [Enflux/SDK/Scenes](Assets/Enflux/SDK/Scenes)

### Enflux - Suit Setup
* This is a scene setup following **Instructions For Setup**

### Enflux - VR Example
* Setup following **VR Setup**, but does not include the required Steam or Oculus packages.

### Enflux - Recording Example 
* Scene including additional recording and playback capability. This can save and play back animations with a character model.
* The scene contains two humanoids, one for recording and one for playback.
* Start animating the recording humanoid using previous instructions.
* (optional) Set the file name in the included UI to save to a meaningful filename and location.
* Use the included UI to start and stop recording and playback.

&nbsp;
## FAQs
------
<b>Q:</b> <i>Can I use different 3D models?</i>

<b>A:</b> Right now, your character must be rigged in the same hierarchy as our provided character with no rotations applied to the limb joints for the `RigMapper` script to work properly. We have successfully tested different rigs/models internally, and it's on our roadmap to add support for other rigs. 


<b>Q:</b> <i>Can I use multiple suits at once?</i>

<b>A:</b> This is not currently supported yet. You're more than free to create a networked experience to use several suits, however. 

&nbsp;
## License And Copyright
------
* Copyright (c) 2017 Enflux Inc.
* By downloading, accessing or using this SDK, you signify that you have read, understood and agree to the terms and conditions of the End User License Agreement located at: https://www.getenflux.com/pages/sdk-eula
* License subject to change
* All code provided **AS IS** with **NO WARRANTY**
* Enflux Inc. is not responsible for lost work from program crashes. 
* **MAKE SURE ALL WORK IS SAVED BEFORE RUNNING**