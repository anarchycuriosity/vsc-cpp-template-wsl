# My C++ Dev Workspace (WSL Optimized)

本项目基于原 `vsc-for-cpp` 模板进行改进，专门针对 **WSL (Ubuntu)** 环境下的后端开发学习进行了优化，同时兼容 Windows MinGW。

## 环境要求 (Environment)

### WSL (Ubuntu) - 推荐方案

- **Compiler**: GCC 13+ (支持 C++23)
- **Debugger**: GDB
- **VS Code Extensions**: 必须在 WSL 内部安装 `C/C++ Extension Pack`。

## 目录结构 (Structure)

- `src/`: 存放 `.cpp` 源文件。
- `inc/`: 存放公共 `.h` 头文件。
- `bin/`: 编译产物存放地。这需要你自己新建

## 快速上手 (Usage)

1. 使用 VS Code 的 **Remote - WSL** 插件连接到子系统。
2. 打开本项目根目录。
3. **编译与调试**：
   - 打开 `src` 下的代码文件。
   - 按 `F5` 启动调试。

## 注意事项

- 本配置已移除原有的 shell 脚本跳转，直接调用系统级 `g++`，更加轻量稳定。
- 默认开启 `-std=c++23` 标准。
- 如果新建bin后编译sample失败请检查WSL的locale中的LANG
- 如果集成终端出现中文乱码或者不显示，首先确保你已经下载好对应的语言包，和设置好locale，然后在vsc的设置(ctrl + ,)搜索terminal > integrated : Detected locale改为off，这可以让集成终端跟着locale的设置走
