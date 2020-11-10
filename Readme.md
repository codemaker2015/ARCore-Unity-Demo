# Technical Steps
1. Make sure you have [Unity](https://store.unity.com/?_ga=2.225845274.1602492542.1529523463-1359490310.1515098122) 2017.2 or higher installed and make sure to include android build support when installing.
2. Download [Android](https://developer.android.com/studio/) Studio.
3. Download [Java Dev Kit](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).
4. Create a new project and then in Unity go to File>Build Settings and select android and click switch platform.
5. Then go to Edit>Preferences then in the prompt click External Tools. Scroll down on until you see SDK and JDK.
6. Click Browse on the JDK and Unity should locate your JDK itself pretty well and you can confirm.
7. Open android studio and then click on configure at the bottom of the prompt and select SDK manager. The android SDK location should appear at the top (if you you have android SDK on the left selected, it is by default) Copy that location for later.
8. Right under the ASK location there is a tab for SDK Tools, click that and then in the list check “Android SDK Build-Tools XX”, “Android SDK Platform-Tools”, “Android SDK Tools”, and click Apply and OK at the bottom of this window.
9. Now go into Unity and return to Edit>Preferences>External Tools and this time click Browse on the SDK and find your android sdk, this is where you can paste your SDK path. By default it is in this directory: `C:\Users\YourUserName\AppData\Local\Android\Sdk`
10. Go to File>Build Settings then click on Player Settings on the bottom left of the prompt. Then in the inspector you should be able to find a section that says Other settings click on that to expand it. Uncheck the option for Multithreaded Rendering.
11. Then go to package name and change that something unique but keep the same structure com.something.something
12. Change the minimum API level to Android 7.0 or higher
13. Then go down to XR settings, expand it and check on ARCore Supported.
14. Download the latest version of [ARCore SDK for Unity](https://github.com/google-ar/arcore-unity-sdk/releases).
15. In Unity click on `Assets>Import Package>Custom Package` and navigate to where you downloaded the ARCore SDK Then import it to Unity.
16. Then navigate in the project tab to the HelloAR Scene. 
17. `GoogleARCore>Examples>HelloAR>Scenes`. Open this scene up.
18. Go to File>Build Settings and click on add open scenes in the prompt.
19. Make sure your mobile device is plugged in, unlocked and prepped for mobile development. Then Build And Run! Save the name. A common problem is that the version of tools Android Studio downloaded for you doesn’t work properly. Download an older version that does from [here](https://developer.android.com/studio). Then go to your Android SDK directory, change the name of the current “tools” folder to something else like “toolsxxxx” and copy paste the tools that you just downloaded into this directory.

# Preparing mobile for development

1. Configure Developer options by activating developer mode. Example for the S7: Settings>System>About>Device>Software>Info then Tap Build number 7 times.
    1. Enable USB Debugging
    2. Allow mock locations
    3. Verify apps via USB
2. Configure Display Options in settings
    1. Disable Lock screen
    2. Set display Timeout. (Lock/security screen to none)
3. For Daydream install Google VR services from the play store
4. For GearVR plug your Samsung phone into the gearVR and follow steps shown to install GearVR services onto your device.