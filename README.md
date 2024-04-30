# Android 多渠道签名工具

该工具基于apktool实现，可以进行多个渠道打包、签名。

# 使用方式
1、请从release下载对应系统的zip文件，如Mac 下载 bindchannels-macos-1.0.0.zip文件  
2、需要Java环境（JDK11+）  
3、配置好Android签名工具环境（zipalign、apksigner）  
4、启动该工具的方式  
4.1、Mac OS命令行运行 start.sh，或双击该文件  
```shell
./start.sh
```
4.1.1、首次执行可能没有权限；还需下面提权操作  
```shell
chmod +x start.sh
```
4.1.2 检查工具执行环境是否正常，会有相关的信息输出；输出信息都是[Y]开头，代表环境正常，否则请修改相关配置  
```shell
./start.sh doctor
```

4.2、Windows命令行运行 start.bat，或双击该文件  
```shell
start.bat
```

4.2.1、检查工具执行环境是否正常，会有相关的信息输出；输出信息都是[Y]开头，代表环境正常，否则请修改相关配置  
```shell
start.bat doctor
```

4.2.2、用户还需要验证apksigner命令是否可用，不可用需要加入下面的配置到keys.yaml中  
```yaml
apkSignerCmd: java -jar apksigner.jar的具体路径
```

# 工具说明
将下载下来的zip文件，放到任意自己喜欢的目录解压。  

首次运行会在jar文件的同级目录创建两个yaml文件，keys.yaml、channel.yaml。详细配置见example  
> keys.yaml 用于配置apk签名需要的参数，目前暂只支持密钥库文件
>  
> channel.yaml 用于配置apk要打的多渠道  

# 现在去试试看吧
