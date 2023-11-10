# LeapMotion Configration

 在 macOS 设备上配置 Leap Motion Controller 到 TouchDesigner

## 概览

- Leap Motion Controller是一款用于手势控制和跟踪的硬件设备，本文档旨在帮助您在TouchDesigner应用程序中成功配置和使用它。
- 本文档提供了连接Leap Motion Controller硬件到macOS设备的详细步骤，适用于不同版本的macOS，包括Catalina和Monterey/Ventura。
- 请根据您的操作系统版本和具体需求，参考相应的部分。


## 硬件设备
- Leap Motion Controller (旧版一代，非新版 Leap Motion Controller 2)

## 步骤

### macOS Catalina

1. 安装 Leap 驱动程序，需要使用可用的旧版 Mac 驱动程式（TRACKING SOFTWARE MAC 2.3.1）。
2. 复制驱动 `libLeap.dylib` 文件（位于 `Leap Motion.app/Contents/Frameworks`）到 TouchDesigner 的 Frameworks文件夹中（`TouchDesigner.app/Contents/Frameworks`）。
3. 打开 TouchDesigner，添加 TD LeapMotion CHOP。
4. 检查数据传输是否正常。

### macOS Monterey/Ventura

1. ***只能使用 TD 2021 版本。***
2. 安装 Leap 驱动程序，需要使用可用的旧版 Mac 驱动程式（TRACKING SOFTWARE MAC 2.3.1）。
3. 复制驱动 `libLeap.dylib` 文件（位于 `Leap Motion.app/Contents/Frameworks`）到 TouchDesigner 的 Frameworks文件夹中（`TouchDesigner.app/Contents/Frameworks`）。
4. 在设备连接状态下打开驱动，然后打开 Leap Motion 控制面板，在 "故障排除" 中选择 "重新校准设备"，***在 "重新校准设备" 界面中重启电脑以激活 Leap Motion。***
5. 重启后，状态栏中的驱动程序应该点亮绿灯。
6. 打开 TouchDesigner，添加 TD LeapMotion CHOP。
7. 检查数据传输是否正常。

## 安装 TouchDesigner 2021 版本

- 在官网下载页 [TouchDesigner Download Archive](https://derivative.ca/download/archive) 选择对应版本进行下载。

## 安装 Leap 驱动

- 需要使用可用的旧版 Mac 驱动程式（TRACKING SOFTWARE MAC 2.3.1）。
- 官方下载链接： [Leap Motion Mac 2.3.1](https://developer.leapmotion.com/releases/mac-2-3-1)。
- 如果在官网下载驱动时遇到 ‘application error" 无法下载驱动，可以尝试通过第三方渠道下载，例如 [TechSpot](https://www.techspot.com/downloads/6701-leap-motion.html)。

## 问题排查

1. 检查您的系统版本。
2. 确保已安装 Leap Motion 的驱动程序。
3. 请注意，不同版本的 macOS 需要不同的方法来启动 Leap Motion，如 Monterey/Ventura ***需要在 Leap 检测界面重启电脑来启动 Leap Motion。***

#### M1 macOS Ventura 用户的额外提示

> 如果您使用 M1 macOS Ventura 按以上方法仍无法正常连接，可以尝试以下步骤进行操作：
>
> 1. 打开 Activity Monitor App。
> 2. 选择网络选项卡。
> 3. 搜索 `UVCAssistant`。
> 4. 选择 "停止"（保持停止直到 Leap Motion 传感器连接）。
