
# Taplytics React Native SDK

_Taplytics is a native mobile A/B testing and push notification platform that helps you optimize your React Native app!_

 [Commercial License / Terms](http://taplytics.com/terms)
 
### **Current Version: [1.0.11](#changelog)**

## 1. Getting Started

**If you haven't yet set up a React-Native project, do the following:**

First install node and react.

1. `brew install node`
2. `brew install watchman`
3. `npm install -g react-native-cli`

Then, initialize a new project.

1.  `react-native init projectname`
2. `cd projectname`
3. `npm install`

#### **To install the taplytics-react-native package:**

* `npm install  taplytics-react-native --save`

Then

* `react-native link taplytics-react-native`


## 2. iOS Setup

1. **[Simply follow part 1. Install from the iOS SDK docs here.](https://github.com/taplytics/taplytics-ios-sdk/blob/master/START.md#1-install)**

## 3. Android Setup

1. Append the `taplytics-react-native` project `settings.gradle` include line:

```gradle
include 'app:', ':taplytics-react-native'
```

2. add the following line to `settings.gradle`
  	
  	
```gradle
project(':taplytics-react-native').projectDir = new File(rootProject.projectDir, 	'../node_modules/taplytics-react-native/android')
```

3. In your app-level `build.gradle` add the following your dependencies:

```      
compile project(':taplytics-react-native')
```

4. In your app-level `build.gradle`, add this the taplytics url to your repositories:

```
    repositories {                                                                                              
        maven { url "https://github.com/taplytics/Taplytics-Android-SDK/raw/master/AndroidStudio/" }
}
```

5. In your Application Class (default is `MainApplication`), add Taplytics to your app's packages:

```
    @Override
    protected List<ReactPackage> getPackages() {
      return Arrays.asList(
          new MainReactPackage(),
          new TaplyticsReactPackage()
      );
   }
```

5. **[Simply follow part 1. Install and part 2. Setup from the Android SDK docs here.](https://github.com/taplytics/taplytics-android-sdk/blob/master/START.md#1-installation)**


## 4. Start making Experiments and sending Push Notifications to your users.

This module wraps most native SDK methods in Javascript, allowing you to access features such as dynamic variables, code blocks and event logging in the React Native environment.

Be sure to import Taplytics into your react application:

```
import Taplytics from 'taplytics-react-native';
```

Then follow the [Experiment](/EXPERIMENTS.md) guide and the [Push Notification](/PUSH.md) guide to get started.

## Changelog


**Current Version: [1.0.11](https://github.com/taplytics/Taplytics-React-Native/releases/tag/1.0.11)**

1. Fixed json attributes passed into logEvent and logRevenue causing crash.

**[1.0.10](https://github.com/taplytics/Taplytics-React-Native/releases/tag/1.0.10)**

1. Fixed search paths for non-cocoapods import

**[1.0.9](https://github.com/taplytics/Taplytics-React-Native/releases/tag/1.0.9)**

1. Fixed getSessionInfo crash

**[1.0.8](https://github.com/taplytics/Taplytics-React-Native/releases/tag/1.0.8)**

1. Added push ID to value sent to BroadcastReceiver


**[1.0.7](https://github.com/taplytics/Taplytics-React-Native/releases/tag/1.0.7)**

1. Added safety in broadcastReceiver

**[1.0.6](https://github.com/taplytics/Taplytics-React-Native/releases/tag/1.0.6)**

1. Fixed broadcastreceiver sending wrong push event types.

**[1.0.5](https://github.com/taplytics/Taplytics-React-Native/releases/tag/1.0.5)**

1. Updated android package name from com.react to com.taplytics.react

**[1.0.4](https://github.com/taplytics/Taplytics-React-Native/releases/tag/1.0.4)**

1. Updated search paths

**[1.0.3](https://github.com/taplytics/Taplytics-React-Native/releases/tag/1.0.3)**

1. Fixed npm references not pointing to the right project.
2. Cleaned up many iOS functions.

**[1.0.1](https://github.com/taplytics/Taplytics-React-Native/releases/tag/1.0.1)**

1. Fixed react native minimum version number. 

**[1.0.0](https://github.com/taplytics/Taplytics-React-Native/releases/tag/1.0.0)**

1. Initial version of React Native SDK. Please contact us with any questions or use git issues. 




