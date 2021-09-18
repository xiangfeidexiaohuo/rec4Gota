# rec4Gota



#### 灵感来源于[android/platform/bootable/recovery/f087dfb/./updater/updater.c](https://android.googlesource.com/platform/bootable/recovery/+/f087dfb/updater/updater.c)


#### 一个简单的小补丁，解决TWRP不能刷超过4G ROM的问题。


***

### 用法：

#### 1.下载[rec4Gota](https://github.com/xiangfeidexiaohuo/rec4Gota/releases)卡刷补丁

#### 2.sdcard根目录建立ota.txt，书写内容：
```
/sdcard/000work/miui_UMI_21.9.17_7b72aa9d01_11.0.zip
/sdcard/000work/magisk.zip

```
![png](./pic/1.png)

ps：

1.刷入/sdcard/000work下的包和magisk。

2.可用#注释不需要刷入的zip。

3.路径可自定义，但是必须是/sdcard/下，不能出现中文目录。

4.仅支持arm64架构。

#### 3.重启进入twrp，刷入该补丁：[rec4Gota](https://github.com/xiangfeidexiaohuo/rec4Gota/releases)。

![png](./pic/2.png)

![png](./pic/3.png)

遇到挂载失败，重启twrp！


***

### 贡献

[SK](https://github.com/sekaiacg)

[yanbuyu](https://github.com/yanbuyu)










