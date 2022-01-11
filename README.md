##欢迎来到 Visual Studio Code Extension for Arduino 预览!Arduino扩展使在Visual Studio Code中轻松开发，构建，部署和调试Arduino草图，并具有一组丰富的功能。这些包括：

Arduino 草图的智能感知和语法突出显示
在Visual Studio Code中验证并上传草图
内置开发板和库管理器
内置示例列表
内置串行监视器
草图的片段
自动Arduino项目脚手架
命令面板 （） 常用命令的集成（例如验证、上传等）F1
集成 Arduino 调试新增功能
##先决条件
需要Arduino IDE或Arduino CLI。

##Arduino IDE
Arduino IDE可以安装在Arduino下载页面。

支持的 Arduino IDE 版本是及更高版本。1.6.x
Windows 应用商店的 Arduino IDE 版本不受支持，因为应用程序在沙盒环境中运行。
注意：Arduino IDE有一些重大更改，导致板包和库安装失败。这些故障在以后得到了纠正。1.8.71.8.8
##Arduino CLI
Arduino CLI可以从存储库的发布页面下载

该扩展仅使用 v0.13.0 进行了测试。
如果使用 CLI，则必须进行设置，因为 CLI 没有默认路径。arduino.path
##安装
打开 VS Code 并按 + + 打开命令面板，选择"安装扩展"并键入 。F1CtrlShiftPvscode-arduino

##或者启动 VS 代码快速打开 （ + ），粘贴以下命令，然后按 Enter。CtrlP

ext install vscode-arduino
您还可以直接从 Visual Studio Code 中的 Marketplace 进行安装，搜索 。Arduino

##立即开始
每次连接受支持的设备时，都可以找到代码示例和教程。或者，您可以访问我们的IoT 开发人员博客空间或入门教程。

##命令
此扩展在命令面板（或 + + ）中提供了几个命令来处理文件：F1CtrlShiftP*.ino

Arduino：董事会经理：管理董事会的软件包。您可以通过在主板管理器中进行配置来添加第三方 Arduino 开发板。Additional Board Manager URLs
Arduino：更改波特率：更改所选串行端口的波特率。
Arduino：更改板类型：更改板类型或平台。
Arduino：关闭串行监视器：停止串行监视器并释放串行端口。
Arduino：示例：显示示例列表。
Arduino：初始化：带有Arduino草图的VS Code项目的脚手架。
Arduino：库管理器：浏览和管理库。
Arduino：打开串行监视器：在集成输出窗口中打开串行监视器。
Arduino：选择串行端口：更改当前串行端口。
Arduino：将文本发送到串行端口：通过当前串行端口发送一行文本。
Arduino：上传：构建草图并上传到Arduino板。
Arduino：CLI 上传：上传没有构建草图的复杂代码（仅限 CLI）。
Arduino：使用编程器上传：使用外部编程器上传。
Arduino：使用程序员进行 CLI 上传：使用外部程序员上传，无需构建草图（仅限 CLI）。
Arduino：验证：构建草图。
Arduino：重新生成智能感知配置：强制/手动重新生成智能感知配置。该扩展分析Arduino的构建输出，并相应地设置IntelliSense包含路径，定义，编译器参数。
键绑定
Arduino： Upload + + orAltCmdU Alt + Ctrl + U
Arduino：验证+ +或AltCmdR Alt + Ctrl + R
Arduino：重建 IntelliSense Configuration + +或AltCmdI Alt + Ctrl + I
##选项
##选择	描述
arduino.path	Arduino 的路径，您可以通过修改此设置以包含完整路径来使用 Arduino 的自定义版本。示例：适用于 Windows、Mac、Linux。（更改后需要重新启动）。从 Arduino IDE 安装路径中自动检测默认值。C:\\Program Files\\Arduino/Applications/home/<username>/Downloads/arduino-1.8.1
arduino.commandPath	相对于 的可执行文件（或脚本）的路径。默认值适用于 Windows、Mac 和 Linux，您还可以通过修改此设置来使用自定义启动脚本来运行 Arduino。（更改后需要重新启动）示例：适用于 Windows、Mac 和 Linux。arduino.patharduino_debug.exeContents/MacOS/Arduinoarduinorun-arduino.batContents/MacOS/run-arduino.shbin/run-arduino.sh
arduino.additionalUrls	第三方软件包的其他主板管理器 URL。您可以在一个字符串中有多个 URL，其中逗号（） 作为分隔符，或者具有一个字符串数组。默认值为空。,
arduino.logLevel	CLI 输出日志级别。可以是信息或详细。缺省值为 。"info"
arduino.allowPDEFiletype	允许 VSCode Arduino 扩展程序从 1.0.0 之前的 Arduino 版本打开 .pde 文件。请注意，这将破坏处理代码。默认值为 。false
arduino.enableUSBDetection	启用/禁用 VSCode Arduino 扩展中的 USB 检测。缺省值为 。当您的设备插入计算机时，它会弹出一条消息""。单击该按钮后，它将自动检测连接USB设备的串行端口（COM）。如果您的设备不支持此功能，请向我们提供您设备的PID / VID;代码格式在 中定义。要了解有关如何列出 vid/pid 的详细信息，请使用以下工具：https://github.com/EmergingTechnologyAdvisors/node-serialporttrueDetected board ****, Would you like to switch to this board typeYesmisc/usbmapping.json npm install -g serialport serialport-list -f jsonline
arduino.disableTestingOpen	启用/禁用自动将测试消息发送到串行端口以检查打开状态。默认值为（将发送测试消息）。false
arduino.skipHeaderProvider	启用/禁用为标头提供完成项的扩展。此功能包含在较新版本的 C++ 扩展中。缺省值为 。false
arduino.defaultBaudRate	串行端口监视器的默认波特率。默认值为 115200。支持的值为 300、1200、2400、4800、9600、19200、38400、57600、74880、115200、230400 和 250000
arduino.disableIntelliSenseAutoGen	当 vscode-arduino 不会通过分析 Arduino 的编译器输出来自动生成 IntelliSense 配置（即 ）时。true.vscode/c_cpp_properties.json
以下 Visual Studio Code 设置可用于 Arduino 扩展。这些可以在全局用户首选项 + 或工作区设置 （） 中设置。后者覆盖了前者。Ctrl,.vscode/settings.json

{
    "arduino.path": "C:/Program Files (x86)/Arduino",
    "arduino.commandPath": "arduino_debug.exe",
    "arduino.logLevel": "info",
    "arduino.allowPDEFiletype": false,
    "arduino.enableUSBDetection": true,
    "arduino.disableTestingOpen": false,
    "arduino.skipHeaderProvider": false,
    "arduino.additionalUrls": [
        "https://raw.githubusercontent.com/VSChina/azureiotdevkit_tools/master/package_azureboard_index.json",
        "http://arduino.esp8266.com/stable/package_esp8266com_index.json"
    ],
    "arduino.defaultBaudRate": 115200
}
注意：您只需要在Visual Studio Code设置中设置，其他选项不是必需的。arduino.path

##以下设置与Arduino扩展的草图设置相同。您可以在工作区下找到它们。.vscode/arduino.json

{
    "sketch": "example.ino",
    "port": "COM5",
    "board": "adafruit:samd:adafruit_feather_m0",
    "output": "../build",
    "debugger": "jlink",
    "prebuild": "./prebuild.sh",
    "postbuild": "./postbuild.sh",
    "intelliSenseGen": "global"
}
sketch- Arduino的主要草图文件名。
port- 连接到设备的串行端口的名称。可以通过命令设置。对于Mac用户来说，可能是"/dev/cu.wchusbserial1420"。Arduino: Select Serial Port
board- 当前选定的Arduino板别名。可以通过命令设置。另外，您可以在那里找到主板列表。Arduino: Change Board Type
output- Arduino构建输出路径。如果未设置，Arduino 每次都会创建一个新的临时输出文件夹，这意味着它无法重用上一个版本的中间结果，从而导致验证/上传时间过长，因此建议设置该字段。Arduino 要求输出路径不应是工作区本身或工作区的子文件夹中，否则可能无法正常工作。默认情况下，不设置此选项。值得注意的是，在构建过程中可能会删除此文件的内容，因此请选择（或创建）一个不会存储要保留的文件的目录。
debugger- 当电路板本身没有调试器并且有多个调试器可用时，将使用的调试器的短名称。您可以在此处找到调试器列表。默认情况下，不设置此选项。
prebuild- 外部命令，将在任何草图构建之前调用（验证，上传等）。有关详细信息，请参阅生成前和生成后命令部分。
postbuild- 在成功构建草图后运行的外部命令。有关更多详细信息，请参阅前面提到的部分。
intelliSenseGen- 覆盖用于自动生成智能感知配置的全局设置（即 ）。有三个选项可用：.vscode/c_cpp_properties.json
"global"：使用全局设置（默认）
"disable"：禁用自动生成，即使全局启用
"enable"：启用自动生成，即使全局禁用
buildPreferences- 设置Arduino首选项，然后在任何构建期间使用（验证，上传等）。这允许额外的定义，编译器选项或包含。必须按如下方式设置首选项键值对：
    "buildPreferences": [
        ["build.extra_flags", "-DMY_DEFINE=666 -DANOTHER_DEFINE=3.14 -Wall"],
        ["compiler.cpp.extra_flags", "-DYET_ANOTER=\"hello\""]
    ]
}
##构建前和构建后命令
在 Windows 上，命令在 -中运行，在 Linux 和 OSX 上在 -实例中运行。因此，您的命令可以是您可以在这些shell中运行的任何命令。您可以调用脚本，而不是运行命令。这使得编写更复杂的构建前/后构建机制变得更加容易，并开辟了运行python或其他脚本语言的可能性。这些命令在工作区根目录中运行，vscode-arduino 设置以下环境变量：VSCA_BUILD_MODE当前生成模式、、或 之一。这仅允许您在某些生成模式下运行脚本。 VSCA_SKETCH 相对于工作空间根目录的草图文件。 VSCA_BOARD 您的主板和配置，例如. VSCA_WORKSPACE_DIR 工作区根目录的绝对路径。 VSCA_LOG_LEVEL 当前日志级别。这使您可以控制脚本的详细程度。 VSCA_SERIAL 用于上传的串行端口。如果未在 中设置，则不设置。 VSCA_BUILD_DIR 生成目录。如果未在 中设置，则不设置。cmdbashVerifyingUploadingUploading (programmer)Analyzingarduino:avr:nano:cpu=atmega328arduino.jsonarduino.json

例如，在 Windows 下，以下设置arduino.json

{
    "board": "arduino:avr:nano",
    "sketch": "test.ino",
    "configuration": "cpu=atmega328",
    "prebuild": "IF \"%VSCA_BUILD_MODE%\"==\"Verifying\" (echo VSCA_BUILD_MODE=%VSCA_BUILD_MODE% && echo VSCA_BOARD=%VSCA_BOARD%)"
}
将产生

[Starting] Verifying sketch 'test.ino'
Running pre-build command: "IF "%VSCA_BUILD_MODE%"=="Verifying" (echo VSCA_BUILD_MODE=%VSCA_BUILD_MODE% && echo VSCA_BOARD=%VSCA_BOARD%)"
VSCA_BUILD_MODE=Verifying
VSCA_BOARD=arduino:avr:nano:cpu=atmega328
Loading configuration...
<...>
验证时。

##智能感知
vscode-arduino 默认自动配置 IntelliSense。vscode-arduino 通过运行单独的构建来分析 Arduino 的编译器输出，并在 中生成相应的配置文件。vscode-arduino尽可能努力地使事情保持最新状态，例如，它在切换电路板或草图时运行分析。.vscode/c_cpp_properties.json

但是重复运行分析是没有意义的。因此，如果工作区报告问题（"波浪线"）（例如，从新库添加新包含后），请手动运行分析：

手动重建： Arduino： 重建 IntelliSense 配置， 键绑定： + +或AltCmdI Alt + Ctrl + I

手动调用分析时，它将忽略任何全局和项目特定的禁用。

##智能感知配置
vscode-arduino 的分析将结果存储为名为 的专用 IntelliSense 配置。当您位于其中一个源文件中时，您必须从状态栏的最右侧选择它，如下所示：Arduino

74001156-cfce8280-496a-11ea-9b9d-7d30c83765c1

此系统允许您设置和使用自己的智能感知配置，与通过 vscode-arduino 提供的自动生成的配置并行。只需将您的配置添加到默认配置中，并将其命名为与默认配置（）不同，例如 ，然后从状态栏或通过命令面板命令C/C++：选择一个配置...c_cpp_properties.jsonArduinoMy awesome configuration

调试 Arduino Code预览
在开始调试 Arduino 代码之前，请阅读本文档，了解在 Visual Studio Code 中调试的基本机制。有关进一步参考，另请参阅在 VSCode 中调试C++。

确保您的Arduino开发板可以与STLink，Jlink或EDBG一起使用。调试支持目前已通过以下主板进行了全面测试：

MXChip 物联网开发人员套件 - AZ3166
Arduino M0 PRO
阿达果 WICED 无线羽毛
阿达果羽毛 M0
Arduino Zero Pro
开始调试的步骤：

##将开发板正确插入开发计算机。对于那些没有板载调试芯片的电路板，您需要使用 STLink 或 JLink 连接器。
转到调试视图（ + + ）。并在源文件中设置断点。CtrlShiftD
按以选择调试环境。F5
当命中断点时，可以在调试侧栏上看到变量并添加要监视的表达式。
要了解有关如何调试Arduino代码的更多信息，请访问我们的团队博客。

##更改日志
有关每个版本中的更改的详细信息，请参阅更改日志。

##支持的操作系统
目前，此扩展支持以下操作系统：

Windows 7 及更高版本（32 位和 64 位）
macOS 10.10 及更高版本
Ubuntu 16.04
正如其他用户所报告的那样，该扩展可能适用于其他Linux发行版，但不能保证。
支持
您可以在问题跟踪器上找到完整的问题列表。您可以提交错误或功能建议，并参与社区驱动的讨论。

##发展
安装先决条件：

##Git
节点.js （>= 12.x）
Npm （>= 6.x）
要运行和开发，请执行以下操作：

##git clone https://github.com/microsoft/vscode-arduino
cd vscode-arduino
跑npm i
跑npm i -g gulp
在 Visual Studio Code 中打开 （code .)
按键进行调试。F5
若要测试，请在 VS Code 中按"启动测试"调试配置。F5

##行为准则
该项目采用了微软开源行为准则。有关更多信息，请参阅行为准则常见问题解答或联系opencode@microsoft.com提出任何其他问题或意见。

##隐私声明
微软企业和开发人员隐私声明描述了此软件的隐私声明。

##许可证
此扩展名根据 MIT许可证 获得许可。有关其他版权声明和条款，请参阅第三方声明文件。

##联系我们
如果您想使用VS Code帮助构建最佳的Arduino体验，可以直接通过giter聊天室与我们联系。
