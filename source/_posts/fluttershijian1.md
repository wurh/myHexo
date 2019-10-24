---
title: Flutter 实践 -- 创建我的APP
date: 2019-10-24 16:31:12
categories: Flutter实践
tags: flutter
---

### Flutter简介:

Flutter是Google在2015年推出的移动UI框架，可快速在iOS和Android上构建高质量的原生用户界面。

Flutter第一次亮相于2015年5月Dart开发者峰会上，初始名字叫做“Sky”，后更名为Flutter，Flutter使用Dart语言开发，Dart是Google于2011年推出的新的计算机编程语言。

### Flutter 特点：

- 快速开发
由于Flutter选用了Dart作为其开发语言，Dart既可以是AOT（Ahead Of Time）编译，也可以是JIT（Just In Time）编译，其JIT编译的特性使Flutter在开发阶段可以达到亚秒级有状态热重载，从而大大提升了开发效率。

- 性能优越
使用自带的高性能渲染引擎（Skia）进行自绘，渲染速度和用户体验堪比原生。

- 富有表现力的精美UI
Flutter内置众多精美的Material Design和Cupertino（iOS风格）小部件，开发者可快速构建精美的用户界面，以提供更好的用户体验。

### 创建我的Flutter 应用

> 创建一个flutter 工程

```bash
 flutter create flutter_myapp
```

> 接着我们进入flutter_myapp 可以查阅flutter 的文件目录架构

### 跑一下安卓和IOS应用吧

插上数据线安卓手机 或者 苹果手机,查看一下当前设备

```bash
  flutter devices
```

安装一下我们的应用吧

```bash
 flutter run
```

接着我们的页面就安装了一个flutter_myapp 的app了

![alt text](https://wurh.github.io/images/blogs/20191024/phone1.jpeg "打开app")

接着进去app

![alt text](https://wurh.github.io/images/blogs/20191024/phone3.jpeg "进去app")

### 换一个logo

我们看到手机上的logo 是flutter 自带的， 如果我想换调 那么怎么办呢？

我们可以先去 [iconfont](https://www.iconfont.cn) 搞个自己的logo

![alt text](https://wurh.github.io/images/blogs/20191024/pc3.png "自己logo")

接着我们可以去[图标工场](https://icon.wuruihong.com)  把logo上传，生成自己的android 和 ios logo

![alt text](https://wurh.github.io/images/blogs/20191024/pc1.png "自己logo")

![alt text](https://wurh.github.io/images/blogs/20191024/pc2.png "自己logo")

最后我们把文件下载，并且导出, android 放在res 目录下， ios 放在ios对应的目录下

我们再重启一下app看看吧

```bash
   flutter run
```
![alt text](https://wurh.github.io/images/blogs/20191024/phone2.jpeg "新的app")

### 把名字换掉

#### android 部分：

-   打开 flutter_myapp/android/app/src/main/AndroidManifest.xml

```xml
<application
        android:name="io.flutter.app.FlutterApplication"
        android:label="flutter_myapp"
        android:icon="@mipmap/ic_launcher">
        <activity
            android:name=".MainActivity"
            android:launchMode="singleTop"
            android:theme="@style/LaunchTheme"
            android:configChanges="orientation|keyboardHidden|keyboard|screenSize|locale|layoutDirection|fontScale|screenLayout|density|uiMode"
            android:hardwareAccelerated="true"
            android:windowSoftInputMode="adjustResize">
            <!-- This keeps the window background of the activity showing
                 until Flutter renders its first frame. It can be removed if
                 there is no splash screen (such as the default splash screen
                 defined in @style/LaunchTheme). -->
            <meta-data
                android:name="io.flutter.app.android.SplashScreenUntilFirstFrame"
                android:value="true" />
            <intent-filter>
                <action android:name="android.intent.action.MAIN"/>
                <category android:name="android.intent.category.LAUNCHER"/>
            </intent-filter>
        </activity>
    </application>
```

替换为

```xml
<application
        android:name="io.flutter.app.FlutterApplication"
        android:label="Flutter样例"
        android:icon="@mipmap/ic_launcher">
        <activity
            android:name=".MainActivity"
            android:launchMode="singleTop"
            android:theme="@style/LaunchTheme"
            android:configChanges="orientation|keyboardHidden|keyboard|screenSize|locale|layoutDirection|fontScale|screenLayout|density|uiMode"
            android:hardwareAccelerated="true"
            android:windowSoftInputMode="adjustResize">
            <!-- This keeps the window background of the activity showing
                 until Flutter renders its first frame. It can be removed if
                 there is no splash screen (such as the default splash screen
                 defined in @style/LaunchTheme). -->
            <meta-data
                android:name="io.flutter.app.android.SplashScreenUntilFirstFrame"
                android:value="true" />
            <intent-filter>
                <action android:name="android.intent.action.MAIN"/>
                <category android:name="android.intent.category.LAUNCHER"/>
            </intent-filter>
        </activity>
    </application>
```

#### ios 部分：

- 打开 /flutter_myapp/ios/Runner

```plist
	<key>CFBundleName</key>
	<string>flutter_myapp</string>
```

替换为:

```plist
	<key>CFBundleName</key>
	<string>Flutter样例</string>
```

接着 再来一遍flutter run 吧 我们就可以看到我们的app 已经换名成功了！！！











