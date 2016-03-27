# react-native-sandbox
A sandbox of react native components

## Setup

```bash
$ npm install -g react-native-cli
```

## Launching the project for Android platform

```bash

# You should have configured your $ANDROID_HOME environment var
# In addition you must have an android device connected
$ $ANDROID-SDK/tools/emulator -netdelay none -netspeed full -avd Nexus_5_API_23
$ cd ./src/
$ react-native run-android
```

### Troubleshooting

#### Exception `Failed to find Build Tools revision 23.0.1`

```
FAILURE: Build failed with an exception.

* What went wrong:
A problem occurred configuring project ':app'.
> failed to find Build Tools revision 23.0.1
```

Update or setup android build tools by running the `android` configuration tool

```
android list sdk -a
```

If you want to use a different version than `23.0.1`, modify `build.gradle`

```
android {
    compileSdkVersion 23
    buildToolsVersion "[BUILD_TOOLS_VERSION]"
```

#### Show the debugger

```
adb shell input keyevent 82
```
