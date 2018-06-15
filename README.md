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
### cmd连接夜模拟器：
#### 错误：adb不是内部或外部命令
1.正确的目录运行：androidStudio\Android\sdk\platform-tools<br>
2.新建Android_Platform_Tools环境变量，并配置%Android_Platform_Tools%到path里面<br>
#### 运行连接
```
    adb.exe connect 127.0.0.1:62001
```

### 运行reactNative项目：
```
    react-native run-android
```
