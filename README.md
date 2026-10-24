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