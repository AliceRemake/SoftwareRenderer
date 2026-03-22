# 2024秋计算机图形学上机作业

[![build](https://github.com/AliceRemake/SoftwareRenderer/actions/workflows/cmake-single-platform.yml/badge.svg)](https://github.com/AliceRemake/SoftwareRenderer/actions/workflows/cmake-single-platform.yml)[![GitHub License](https://img.shields.io/github/license/AliceRemake/SoftwareRenderer)](https://github.com/AliceRemake/SoftwareRenderer/blob/main/LICENSE)

![main.png](./Image/main.png)

## 工具链和平台

| 工具链                                                                                     | 平台                                                         |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [![Static Badge](https://img.shields.io/badge/MinGW-green)](https://www.mingw-w64.org/) | ![Static Badge](https://img.shields.io/badge/Windows-blue) |

## 克隆仓库

```bash
git clone --recursive https://github.com/AliceRemake/SoftwareRenderer.git
```

## 编译

```bash
mkdir build && cd build
cmake -G "MinGW Makefiles" -DCMAKE_BUILD_TYPE=Release ..
mingw32-make -j16
```

## 第三方库

* SDL：管理窗口和绘制imgui
* imgui：UI
* fmt：格式化库
* glm：向量库

## 功能

* 显示包围盒，面法线和ZBuffer
* 背面剔除
* 视域四棱锥裁剪
* 消隐算法
  * 简单的ZBuffer算法
  * 简单的层次ZBuffer算法
  * 层次ZBuffer算法 + 层次包围盒
* 基本的建模功能
  * 可以导入模型，调整模型，可以支持多边形网格
  * 可以导入光源（平行光、点光源），调整光源
  * 可以调整、移动相机
  * 可以调整光照模型

![teapot](./Image/teapot.png)

![wireframe](./Image/wireframe.png)

![normal](./Image/normal.png)

![AABB](./Image/AABB.png)

![ZBuffer](./Image/ZBuffer.png)
