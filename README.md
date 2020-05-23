# android-i2ctool
移植 开源的 i2c-tools-4.1 到 Android 设备
代码均为 开源的 i2c-tools-4.1 备份bin方便使用
### 编译
进入clone的目录 可放入 external/
mm .
### 内容
    i2cdetect – 用來列举I2C bus和上面所有的裝置
    i2cdump – 显示裝置上所有register的值
    i2cget – 获取设备上某个register的值
    i2cset – 写入设备上某个register

i2cdetect 其中 uu 代表被占用，有程序在操作，不一定是有设备连接上了。
真正i2cdetect 发现的是显示设备地址的数据（必然要先保证没有驱动程序占用了该总线上此地址，方能发送和探测否则出现uu）。

使用方法 i2cdetect help 即可
### 依赖
通过操作  /dev 路径 i2c-× 设备文件完成。
请务必kernel 开启
CONFIG_I2C_CHARDEV





