# rec4Gota



#### 灵感来源于[android/platform/bootable/recovery/f087dfb/./updater/updater.c](https://android.googlesource.com/platform/bootable/recovery/+/f087dfb/updater/updater.c)


#### 一个简单的小补丁，解决TWRP不能刷超过4G ROM的问题。

 * 当然没超过4G的ROM也可以用这种方法刷，只不过没必要而已！


#### 更新日志：

* 1.3：支持usb-otg！

* 1.2：完成，开始公测！

***


### 科普下何为超过4G：

 * 请用电脑查看大小，比如下图，10S的包就超过 4G了，K40没超过。

![png](./pic/01.png)

![png](./pic/02.png)


 * 手机上查看大小请用MT管理器。某些人抖机灵，用自带的文件管理，是个很傻的行为。
 
 * 厂商的文件管理是1G按照1000算的，很多包实际没超过4G，但是用自带的文件管理看就超过4G，这种是不准的。

 * 比如K40，包没超过4G，但是用自带文件管理看，都4.25G了。

![png](./pic/03.png)

![png](./pic/04.png)



***

### 用法：

#### 1.下载[rec4Gota](https://github.com/xiangfeidexiaohuo/rec4Gota/releases)卡刷补丁

#### 2.sdcard根目录或者otg设备根目录建立ota.txt，书写内容示例：
```
/sdcard/miui_THYME_21.9.17_411bcbbac6_11.0.zip
/sdcard/magisk.zip

```
![png](./pic/05.png)

 * sdcard根目录的ota.txt优先级最高，若otg设备也存在ota.txt，只会读取sdcard里的ota.txt。

 * 若你要把ROM放在otg设备里，那么ota.txt书写内容示例：
```
/usb-otg/miui_THYME_21.9.17_411bcbbac6_11.0.zip
/usb-otg/magisk.zip

```
![png](./pic/06.png)


**说明：**

 * 路径可自定义，但是必须是/sdcard/或者/usb-otg/下，不能出现中文目录。

 * 可用#注释不需要刷入的zip。

 * 仅支持arm64架构。

 * 若使用otg设备，请确认在twrp下，otg设备的路径为/usb-otg/，某些私人订制的twrp可能不是这个路径，那么不支持！

#### 3.重启进入twrp，刷入该补丁：[rec4Gota](https://github.com/xiangfeidexiaohuo/rec4Gota/releases)，就会一起刷入ota.txt路径里的ROM/补丁。

 * 示例为小米10这种ROM没超过4G的也能兼容，也能刷！

![png](./pic/07.png)

![png](./pic/08.png)

 * 遇到挂载失败，重启twrp！


***

### 贡献

 * [SK](https://github.com/sekaiacg)

 * [yanbuyu](https://github.com/yanbuyu)




