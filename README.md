这是一个集成了 web3.js 和 ethers.js 的项目案例

# 环境准备
   预备知识：
 > 1. 本项目基于 React Native 0.63.4 版本，如果你还不熟悉 React Native，请先阅读[官方文档](https://reactnative.dev/docs/getting-started)。
 > 
 > 2. 本项目使用 web3.js 1.10.0 版本，如果你还不熟悉 web3.js，请先阅读[官方文档](https://web3js.readthedocs.io/en/v1.10.0/)。
 > 3. 本项目使用 ethers.js 5.0.3 版本，如果你还不熟悉 ethers.js，请先阅读[官方文档](https://docs.ethers.io/v5/)。
 > 4. blockchain 相关知识，如果你还不了解，请先阅读[区块链白皮书](https://bitcoin.org/bitcoin.pdf)。
 > 5. 本项目默认使用者具备前端技术js、nodejs、npm、yarn 等相关知识
 > 6. 请确认是否安装 [RN 基础环境](https://reactnative.dev/docs/environment-setup)


# 如果想使用本项目作为脚手架可以执行以下命令

## 1. 使用项目模板创建项目
```bash
npx react-native-rename@latest "your_project_name"
# your_project_name项目的根文件夹，根据需要自行修改
```

## 2: 安装依赖

```bash
# 使用 npm
npm install
# 或者使用 Yarn
yarn install
```
## 3：启动metro bundler

```bash
# using npm
npm start

# OR using Yarn
yarn start
```

##  4: 启动模拟器或真机

###  Android

```bash
# using npm
npm run android

# OR using Yarn
yarn android
```

###  iOS

```bash
# using npm
npm run ios

# OR using Yarn
yarn ios
```


# 5: 编辑项目

1. Open `App.tsx` in your text editor of choice and edit some lines.
1. 打开 `App.tsx` 文件，编辑其中一些代码。
2. For **Android**: Press the <kbd>R</kbd> key twice or select **"Reload"** from the **Developer Menu** (<kbd>Ctrl</kbd> + <kbd>M</kbd> (on Window and Linux) or <kbd>Cmd ⌘</kbd> + <kbd>M</kbd> (on macOS)) to see your changes!
2. **Android**: 按两次 <kbd>R</kbd> 键或者从 **Developer Menu** 中选择 **"Reload"** 
   (<kbd>Ctrl</kbd> + <kbd>M</kbd> (在 Windows 和 Linux 上) 或 <kbd>Cmd ⌘</kbd> + <kbd>M</kbd> (在 macOS 上))来查看你的修改！

    **iOS**: 在 iOS 模拟器中按 <kbd>Cmd ⌘</kbd> + <kbd>R</kbd> 来重新加载应用并查看你的修改！
# Troubleshooting

## 1.react-native-os react-native-tcp 编译不通过

解决方法：
修改 react-native-os 项目的 build.gradle compile 为 implementation

最终修改

```
yarn add @metamask/react-native-tcp
yarn add @vmagination/react-native-os
```

## 2.程序包 react-native-tcp android.support.annotation 不存在

android.support.annotation.Nullable; 不存在

解决方法：
在 build.gradle 文件添加以下依赖：

```
dependencies {
   implementation 'androidx.annotation:annotation:1.1.0'
}
```

方法二
在 1 中已经解决

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

### 针对 3. 问题 可以采用以下方法更好

升级依赖此项目的模块
执行更新

```bash
yarn add react-native-udp
```

# Learn More

报错引用的文章

[1.android.support.annotation 不存在](https://blog.csdn.net/liting870907/article/details/121158951)

[2.wifi.WifiManager 不存在](https://blog.csdn.net/niudaly/article/details/27678395)

[3.ios 编译 failed](https://levelup.gitconnected.com/tutorial-how-to-set-up-web3js-1-x-with-react-native-0-6x-2021-467b2e0c94a4)
