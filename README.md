## 安装
1.Python2.7<br>
2.Node.js<br>
3.JDK（8.0版本）<br>
4.Android Stdio<br>
5.运行命令(将npm下载的地址转为国内的地址，加快下载速度)
```
     npm config set registry https://registry.npm.taobao.org --global 
     npm config set disturl https://npm.taobao.org/dist --global

     npm install -g react-native-cli // 全局安装react-native-cli
     react-native init MyProject // 初始化一个react-native项目
```



## 运行
### 1.cmd连接夜模拟器：
```
    adb.exe connect 127.0.0.1:62001
```

### 2.运行reactNative项目：
```
    react-native run-android
```

## 错误
### 1.adb不是内部或外部命令
#### 解决办法
方法1.正确的目录运行：androidStudio\Android\sdk\platform-tools<br>
方法2.新建Android_Platform_Tools环境变量，并配置%Android_Platform_Tools%到path里面<br>

### 2.Cannot find entry file index.android.js in any of the roots
在react native以前的版本，index.android.js与index.ios.js是分开的两个文件，在最新版本中这两个文件合并成index.js一个文件了。但是如果你在创建项目之后直接运行，肯定会报Cannot find entry file index.android.js in any of the roots这种类似的错误，因为在根目录下已经不存在index.anroid.js和index.ios.js这两个文件，所以肯定不会检索到，你更改App.js的内容后更不可能生效。
#### 解决办法 https://blog.csdn.net/murdererlingdu/article/details/79788880
```
通过执行
react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res/
命令会在assets目录下生成两个文件
```
