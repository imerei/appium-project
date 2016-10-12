#### tutorial [![Build Status](https://travis-ci.org/appium/tutorial.svg?branch=master)](https://travis-ci.org/appium/tutorial) [![Dependency Status](https://gemnasium.com/appium/tutorial.svg)](https://gemnasium.com/appium/tutorial)

Getting started tutorials for appium

#### 4 Tracks

0. [Ruby Appium iOS](/modules/en/source/appium/01_native_ios_automation)
0. [Ruby Appium Android](/modules/en/source/appium/02_native_android_automation)

Each track is self contained.

Published on [GitHub Pages](https://github.com/appium/tutorial/tree/gh-pages)

### Dependencies
The following prerequisites are needed to run the script: [Homebrew](http://brew.sh/), [Java JDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) (Version 7 or higher), [Android Studio](https://developer.android.com/sdk/index.html), [Appium](http://appium.io/), [Maven](http://maven.apache.org/), and a Nexus 7 tablet configured for testing.
  
<b>Downloading and Installing Homebrew:</b>

  1. Open the Terminal and enter the following command:

        $ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    
  2. While in the Terminal, run <b>brew help</b> to verify that Homebrew is installed.
  
<b>Downloading and Installing Java JDK:</b>

  1. Go to Oracle's [Downloads link](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).
  2. Click on Accept License Agreement.
  3. Select the corresponding .dmg version for Mac OSX 64.
  4. After the download is complete, double click on the .dmg file and follow the instructions to install Java JDK.
  
<b>Downloading and Installing Android Command Line Tools:</b>

  1. Open the Terminal and enter the following command:
  
        $ brew install android-sdk
        
  2. Verify the Android command is installed by entered <b>android -h</b>
  3. While in the Terminal, enter the following command to install the <b>platform-tools</b>:
  
        $ android update sdk --no-ui --filter 'platform-tools'
  
  4. Verify <b>platform-tools</b> were installed correctly by entering <b>adb version</b>.
  5. While in the Terminal, enter the following command to yield the list of sdk packages:
  
        $ android list sdk --all
        
  6. Find <b>Android SDK Build-tools, revision 22.0.1 or higher</b> and note its number on the list.
  7. While in the Terminal, enter the following command install the <b>build-tools</b>:
  
        $ android update sdk -u --all --filter n (where n is the number on the previously retrieved list)
  
  8. When prompted, enter <b>Y</b> to accept the license and press Enter<Return>.
  
<b>Downloading and installing Appium Command Line Tools:</b>

  1. Open the terminal and enter the following command:
  
        $ npm install -g appium
  
  2. After the download is complete, enter the following command:
  
        $ appium &
  
  3. While in the Terminal, confirm the appium cammond is available by entering <b>appium -v</b>.

<b>Downloading and Installing Maven:</b>

  1. Open the Terminal and enter the following command:
  
        $ brew install maven

  2. While in the Terminal, run <b>mvn --version</b> to verify that it is correctly installed.

#### Running a quick test

  1. Create an Android virtual device (AVD) by following the instructions [here](https://developer.android.com/studio/run/managing-avds.html)
  2. Launch your AVD
  3. Open your Terminal and enter the following command to confirm the AVD is recognized:

	$ adb devices
	
  4. In the Terminal create a new tab and enter "appium" to run the server
  5. In the Terminal create a new tab and change directory to tutorial/projects/java_android
  6. While in the java_android directory, enter to followoing to run the Appium tests

	$ mvn clean test≈
