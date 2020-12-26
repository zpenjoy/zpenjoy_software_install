# CentOS环境下安装JDK1.8

## 总体流程
1. 复制源文件到/usr/local 通过WCP复制文件即可。
2. 解压源文件
3. 配置环境变量
4. 重新加载配置文件
5. 验证

## 文件解压
```sh
tar -zxvf jdk-8u231-linux-x64.tar.gz
```
## 配置环境变量
```sh
vi /etc/profile
##将下列配置填写到环境变量中 放在最后一行即可
#java
export JAVA_HOME=/usr/local/jdk1.8.0_231
export PATH=$JAVA_HOME/bin:$PATH
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib
```
## 重新加载配置文件
```sh
source /etc/profile
```
## 验证

```sh
java -versioin #验证
```
输出如下结果表明JDK安装成功：
>  java version "1.8.0_231"
> Java(TM) SE Runtime Environment (build 1.8.0_231-b11)
> Java HotSpot(TM) 64-Bit Server VM (build 25.231-b11, mixed mode)
