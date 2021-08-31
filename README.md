# install android studio with unreal engine

**get android studio ->** [https://redirector.gvt1.com/edgedl/android/studio/install/2020.3.1.23/android-studio-2020.3.1.23-windows.exe](https://redirector.gvt1.com/edgedl/android/studio/install/2020.3.1.23/android-studio-2020.3.1.23-windows.exe)

**jdk ->** [https://download.oracle.com/otn-pub/java/jdk/16.0.2%2B7/d4a915d82b4c4fbb9bde534da945d746/jdk-16.0.2_windows-x64_bin.exe](https://download.oracle.com/otn-pub/java/jdk/16.0.2%2B7/d4a915d82b4c4fbb9bde534da945d746/jdk-16.0.2_windows-x64_bin.exe)

**jre ->** [https://sdlc-esd.oracle.com/ESD6/JSCDL/jdk/8u301-b09/d3c52aa6bfa54d3ca74e617f18309292/JavaSetup8u301.exe?GroupName=JSC&FilePath=/ESD6/JSCDL/jdk/8u301-b09/d3c52aa6bfa54d3ca74e617f18309292/JavaSetup8u301.exe&BHost=javadl.sun.com&File=JavaSetup8u301.exe&AuthParam=1630432838_66af34fc43eb4672fa5c1defb34a98fb&ext=.exe](https://sdlc-esd.oracle.com/ESD6/JSCDL/jdk/8u301-b09/d3c52aa6bfa54d3ca74e617f18309292/JavaSetup8u301.exe?GroupName=JSC&FilePath=/ESD6/JSCDL/jdk/8u301-b09/d3c52aa6bfa54d3ca74e617f18309292/JavaSetup8u301.exe&BHost=javadl.sun.com&File=JavaSetup8u301.exe&AuthParam=1630432838_66af34fc43eb4672fa5c1defb34a98fb&ext=.exe)

**set JAVA_HOME in env variables:**

`C:\Program Files\Java\jre1.8.0_301`

**Unreal Engine:**

open `UE_4.27\Engine\Extras\Android`

run `SetupAndroid.bat`

**connect ur android device to PC**

on android device open: `Developer options -> USB debugging -> ON`

**after that in Unreal Engine:**

check if ur device appeared in device manager

open `Launch Options -> Device Manager`

ur android device should be on a list.

then open `Project Settings -> Android`

and check if button `"Accept SDK License"` are gray, if not accept it by pressing the button

then change in "Android Package Name" `com.(ur company name).(ur project name)`

then check **Android SDK tab**:

in **SDKconfig**

all lines should be filled with actual paths, example:

Location of Android SDK: `C:/Users/%username%/AppData/Local/Android/Sdk`

Location of Android NDK: `C:/Users/%username%/AppData/Local/Android/Sdk/ndk/23.0.7599858`

Location of java: `C:/Program Files/Java/jre1.8.0_301`

SDK API Level: `latest`

NDK API Level: `android-21`

now u are ready to go, u can launch a game on ur android device

if u got an `error` about corrupted **build-tools, gradle**

u must manually rename these files:

`C:\Users\%username%\AppData\Local\Android\Sdk\build-tools\31.0.0`

from `d8.bat` to `dx.bat`

and 

`C:\Users\%username%\AppData\Local\Android\Sdk\build-tools\31.0.0\lib`

from `d8.jar` to `dx.jar`

now u can assemble ur project for ur android device and test it.


