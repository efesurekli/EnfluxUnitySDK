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
3. Under the tab Assets select Import Package > Custom Package.
4. Navigate to folder containing `Enflux.unitypackage` and select package.
5. A window will open, select Import.
6. Under Project tab, expand Enflux > SDK > Prefabs
7. Drag and drop the following into Hierarchy:
  * [EnfluxManager]
  * [EnfluxHumanoid]
8. If one is not already in the project, add a Canvas.
  * From Enflux > SDK > Prefabs > UI, drag [EnfluxExampleConnectionPanel] onto Canvas.
9. Move camera and [EnfluxExampleConnectionPanel] as needed.

&nbsp;
## Instructions For Setup With VR
------
### HTC Vive Requirements
1. Obtain and import [SteamVR Unity SDK](https://www.assetstore.unity3d.com/en/#!/content/32647)

### Oculus Rift Requirements
1. Obtain and import [Oculus Unity SDK](https://developer3.oculus.com/downloads/)

### VR Setup
1. Replace the [EnfluxHumanoid] prefab with [EnfluxVRHumanoid] prefab.
2. In the "HMD Adapter" component, drag the main camera to the field "HMD".
3. The humanoid will now follow the camera, where the head is placed at the camera location.
4. Lower the camera's near clipping plane close to zero.
4. In Edit > Project Settings > Player make sure "Virtual Reality Supported" is on.

&nbsp;
## Connection Instructions And Issues
------
1. Turn on the Enflux modules you plan to use. In Windows bluetooth manager, click "Pair" on all Enflux modules you wish to use.
2. Run Unity project.
3. Under the "Connect" menu, click shirt and pants to connect to the given modules.
4. If first time using suit or change in environment, click calibrate.
  * [Calibration Tutorial](https://youtu.be/HKrl9DVYESI)
5. The module will initialize for around 2 seconds. **USER NEEDS TO BE STANDING STILL FOR MOST ACCURACY.**
6. When the countdown has completed, the suit should be animating.
7.  When done using the suit, select Disconnect.

* If the module's name is unknown or incorrect, use tools SetShirt.exe or SetPants.exe to correctly asign the module.
* If the module is unable to connect, it may have went to sleep. Try turning it back on.
* If the module is still unable to connect, hard reset the module. Unpair from the module in Windows and reconnect.

### Troubleshooting Guide 
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
## License And Copyright
------
* Copyright (c) 2017 Enflux Inc.
* By downloading, accessing or using this SDK, you signify that you have read, understood and agree to the terms and conditions of the End User License Agreement located at: https://www.getenflux.com/pages/sdk-eula
* License subject to change
* All code provided **AS IS** with **NO WARRANTY**
* Enflux Inc. is not responsible for lost work from program crashes. 
* **MAKE SURE ALL WORK IS SAVED BEFORE RUNNING**