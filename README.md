# Android 多渠道签名工具

该工具基于apktool实现，可以进行多个渠道打包、签名。

# 使用方式
1、下载对应系统的jar文件，如Mac 下载 bindchannels-macos-x64-1.0.0.jar文件  
2、需要Java环境（JDK11+）  
3、配置好Android签名工具环境（apksigner）  
4、启动该工具的命令  
4.1、命令行启动或者脚本启动
```shell
java -jar bindchannels-xxx.jar
```
4.2、Windows可以双击jar包，如果运行不了请使用命令行方式3.1

# 工具说明
将下载下来的jar文件，放到任意自己喜欢的目录；最好是新建一个目录。  

首次运行会在jar文件的上级目录创建两个yaml文件，keys.yaml、channel.yaml。详细配置见example  
> keys.yaml 用于配置apk签名需要的参数，目前暂只支持密钥库文件
>  
> channel.yaml 用于配置apk要打的多渠道  

# 现在去试试看吧
