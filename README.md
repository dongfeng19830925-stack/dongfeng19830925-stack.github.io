# ESP 小实验室

面向 ESP32 的小型示例与实验记录，当前开发目标为 **ESP32-S3**，使用 **ESP-IDF**。

## 示例计划

- GPIO：LED 闪烁、按键输入
- Wi-Fi：扫描附近网络
- HTTP：通过网页查看或控制开发板

每个完成的示例会补充源码、接线说明、构建与烧录命令。网站首页由 `index.html` 提供，通过 GitHub Pages 发布。

## 本地开发

在 ESP-IDF Terminal 中进入相应示例目录，然后运行：

```powershell
idf.py set-target esp32s3
idf.py build
idf.py -p COMx flash monitor
```

把 `COMx` 替换成设备管理器中实际的串口号。烧录会改写开发板 Flash。

## 网站

GitHub Pages 地址：<https://dongfeng19830925-stack.github.io/>
## BLE 网页连接 Demo

- 网页控制台：https://dongfeng19830925-stack.github.io/ble/
- 固件工程（私有）：https://github.com/dongfeng19830925-stack/esp32-ble-web
- ESP32-S3 作为 NimBLE GATT 外设，网页通过 Web Bluetooth 连接附近设备并读写控制特征值。
- ON/OFF 是逻辑状态演示；当前不会驱动 GPIO。设备需要先烧录固件。
- 浏览器需支持 Web Bluetooth；页面用 HTTPS，设备发现由用户点击触发。浏览器必须能直连附近蓝牙设备，不能远程跨网访问蓝牙。