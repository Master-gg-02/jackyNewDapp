This is a new [**React Native**](https://reactnative.dev) project, bootstrapped using [`@react-native-community/cli`](https://github.com/react-native-community/cli).

# Getting Started

> **Note**: Make sure you have completed the [React Native - Environment Setup](https://reactnative.dev/docs/environment-setup) instructions till "Creating a new application" step, before proceeding.

## Step 1: Start the Metro Server

First, you will need to start **Metro**, the JavaScript _bundler_ that ships _with_ React Native.

To start Metro, run the following command from the _root_ of your React Native project:

```bash
# using npm
npm start

# OR using Yarn
yarn start
```

## Step 2: Start your Application

Let Metro Bundler run in its _own_ terminal. Open a _new_ terminal from the _root_ of your React Native project. Run the following command to start your _Android_ or _iOS_ app:

### For Android

```bash
# using npm
npm run android

# OR using Yarn
yarn android
```

### For iOS

```bash
# using npm
npm run ios

# OR using Yarn
yarn ios
```

If everything is set up _correctly_, you should see your new app running in your _Android Emulator_ or _iOS Simulator_ shortly provided you have set up your emulator/simulator correctly.

This is one way to run your app — you can also run it directly from within Android Studio and Xcode respectively.

## Step 3: Modifying your App

Now that you have successfully run the app, let's modify it.

1. Open `App.tsx` in your text editor of choice and edit some lines.
2. For **Android**: Press the <kbd>R</kbd> key twice or select **"Reload"** from the **Developer Menu** (<kbd>Ctrl</kbd> + <kbd>M</kbd> (on Window and Linux) or <kbd>Cmd ⌘</kbd> + <kbd>M</kbd> (on macOS)) to see your changes!

   For **iOS**: Hit <kbd>Cmd ⌘</kbd> + <kbd>R</kbd> in your iOS Simulator to reload the app and see your changes!

# Troubleshooting

## 1.react-native-os 编译不通过

解决方法：
修改 react-native-os 项目的 build.gradle compile 为 implementation

## 2.程序包 android.support.annotation 不存在

android.support.annotation.Nullable; 不存在

解决方法：
在 build.gradle 文件添加以下依赖：

```
dependencies {
   implementation 'androidx.annotation:annotation:1.1.0'
}
```

在代码中将相关引用改为

```
import androidx.annotation.Nullable;
```

## 2.wifi.WifiManager 不存在

解决方法：

```
import android.content.Context;
import android.net.wifi.WifiInfo;
import android.net.wifi.WifiManager;
```

### 针对 2.3. 问题 可以采用以下方法更好

升级依赖此项目的模块
执行更新

```
yarn add react-native-tcp
yarn add react-native-udp
```

# Note

该项目仅支持 web3js.1.10 以下的版本

# Learn More

报错引用的文章

[1.android.support.annotation 不存在](https://blog.csdn.net/liting870907/article/details/121158951)

[2.wifi.WifiManager 不存在](https://blog.csdn.net/niudaly/article/details/27678395)

[3.ios 编译 failed](https://levelup.gitconnected.com/tutorial-how-to-set-up-web3js-1-x-with-react-native-0-6x-2021-467b2e0c94a4)
