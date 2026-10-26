# 7kaa Extended Screen Version / 7kaa 高分辨率扩展版

## 项目简介 / Project Introduction

### 中文
《七个王国：远古敌人》(Seven Kingdoms: Ancient Adversaries, 简称 7kaa) 是 1997 年发行的经典即时战略游戏。原版游戏仅支持 800x600 分辨率，在现代高分辨率显示屏上体验不佳（画面过小或拉伸模糊）。

本项目基于官方 2.15.6 版源码，移植了 Android 社区的高分辨率补丁，让游戏能够在现代显示器上原生运行，支持 1920x1080、2560x1440、3840x2160 等分辨率。

**特点：**
- 支持多种分辨率（800x600 至 3840x2160）
- 保持原版 UI 大小，地图区域显示更多内容
- 兼容原版游戏数据文件
- 绿色免安装，解压即用

### English
Seven Kingdoms: Ancient Adversaries (7kaa) is a classic real-time strategy game released in 1997. The original only supports 800x600 resolution, which performs poorly on modern high-resolution displays (too small or stretched/blurry).

This project is based on the official 2.15.6 source code, with the Android community's high-resolution patch ported to enable native high-resolution support for modern displays (1920x1080, 2560x1440, 3840x2160, etc.).

**Features:**
- Multiple resolutions supported (800x600 to 3840x2160)
- Original UI size maintained, map area shows more content
- Compatible with original game data files
- Portable, no installation required

---

## 使用方法 / Usage

### Linux 版 / Linux Version

#### 方法一：绿色运行（推荐）/ Method 1: Portable (Recommended)

```bash
# 1. 解压 / Extract
tar -xzf 7kaa_hd_linux.tar.gz
cd 7kaa_hd_linux/data

# 2. 运行 / Run
./7kaa_hd
```

#### 方法二：系统安装 / Method 2: System Install

```bash
# 运行安装脚本 / Run install script
cd 7kaa_hd_linux
./install.sh
```

安装后可通过桌面图标或命令 `7kaa_hd` 启动。

#### 配置分辨率 / Configure Resolution

编辑 `data/config.ini`：
```ini
# 分辨率设置 / Resolution settings
vga_resolution_width=1920
vga_resolution_height=1080
```

支持的分辨率 / Supported resolutions:
- 800x600（原版 / Original）
- 1280x720（HD）
- 1920x1080（Full HD，默认 / Default）
- 2560x1440（2K）
- 3840x2160（4K）

---

## 构建源码 / Build from Source

### Linux

```bash
# 1. 安装依赖 / Install dependencies (Ubuntu/Debian)
sudo apt install build-essential libsdl2-dev libopenal-dev libenet-dev libcurl4-openssl-dev

# 2. 编译 / Build
cd src
./autogen.sh
./configure
make

# 3. 运行 / Run
./7kaa
```

---

## 技术说明 / Technical Details

本项目基于以下开源项目：
- [7kaa 官方源码](https://7kfans.com/) (GPL v2)
- [Android 社区高清补丁](https://github.com/) (GPL v2)

关键技术：
- 使用原版 800x600 资源，通过镜像平铺（mirror-tiling）技术填充高分辨率屏幕
- 无需高清资源文件，保持兼容性
- UI 元素保持原大小，地图区域根据分辨率扩展

This project is based on:
- [7kaa official source code](https://7kfans.com/) (GPL v2)
- [Android community HD patch](https://github.com/) (GPL v2)

Key technologies:
- Uses original 800x600 resources with mirror-tiling to fill high-resolution screens
- No HD resource files required, maintaining compatibility
- UI elements remain original size, map area expands based on resolution

---

## 许可 / License

GPL v2（与原版 7kaa 相同 / Same as original 7kaa）

---

## 版本历史 / Version History

- **2.15.6EX** (2026-10-26): 首个发布版，支持高分辨率 / First release with high-resolution support

---

## 贡献 / Contributing

欢迎提交 Issue 和 Pull Request！/ Issues and Pull Requests are welcome!

---

## 联系方式 / Contact

GitHub: [7kaa_extended_screen_version](https://github.com/woodgreat/7kaa_extended_screen_version)
