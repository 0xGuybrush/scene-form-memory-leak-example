# SceneForm memory leak example

## Steps to reproduce

### 1. Build and install 

With a device connected to Android Debug Bridge.

```bash
./gradlew assembleDebug
adb install app/build/outputs/apk/debug/app-debug.apk
```

Using the debug variant to capture leak info

### 2. Run the application

* Open the app on your device.
* Click the "next" button when the Main Activity loads
* The AR activity will open
  * Allow camera permissions
  * Move phone to detect planes
* When the "floating hand" icon has disappeared (planes detected), click the "Back" FAB to return to the main activity

## Current outcome

After a couple of seconds, Leak Canary will highlight a leak detected

## Desired outcome

No leak! :) 
