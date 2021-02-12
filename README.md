[中文](./README.md)　|　[English](./README_en.md) 

[Gitee](https://gitee.com/haujet/ali-audio-to-srt.git)　|　[Github](https://github.com/HaujetZhao/ali-audio-to-srt) 

# 阿里云音频转字幕

## ⭐ 简介

功能： 使用阿里云智能语音服务中的录音文件识别 API，实现将视频、音频文件转写出 srt 字幕

下载：

- 发行版下载地址： [Releases](../../releases) 

## 📝 背景

QuickCut 上的转字幕效果不好，有的句子太长，需要优化，但没时间做 GUI，所以做了这个命令行工具。

使用后，会自动生成 `config.ini` 配置文件，请根据提示，在配置文件里填写上阿里云 API 相关参数。

## ✨ 特性

两种运行方式：

* 直接运行，文字引导
* 命令行运行

## 🛠️ 安装

### 📦 发行版

需要提前安装上 FFmpeg

已为 Windows 64 位打包成可直接双击运行的包，请到 [本仓库的 Releases](../../releases) 界面下载。将 7z 压缩包解压后，文件夹内有一个 exe 文件，双击即可运行。 

也可以从命令行运行：

```
ali-audio-to-srt
```

我没有其他系统（例如 Linux、MacOS）的电脑，所以无法为其他系统打包，这些系统的用户需要从源代码或 pip 安装使用。（参见下文）

### ⚙️ 用 pip 安装运行

需要提前安装上 FFmpeg 和 Python3

#### 用 pip 从 pypi 安装

还未上传

#### 用 pip 从源代码安装

将仓库克隆下来，进入仓库文件夹，运行：

```
pip install .
```

就安装上了。然后就可以运行以下命令使用了：

```
ali-audio-to-srt
```

### 📄 从源代码直接运行

将仓库克隆下来，进入仓库文件夹，先安装依赖库：

```
pip install -r requirements.txt
```

然后就可以以模块的方式运行：

```
python -m ali_audio_to_srt
```

## 💡 使用

```
python -m ali_audio_to_srt
```

```shell
python -m ali_audio_to_srt 音频1.mp3 视频2.mkv
```

第一种方式是直接运行，会有文字提示引导你：

```
> python -m ali_audio_to_srt

```

第二种方式是命令行传递参数运行：

```
> python -m ali_audio_to_srt -h
usage: __main__.py [-h] [--version] [-l 语言] Media [Media ...]

功能：使用阿里云的录音文件识别服务将视频或音频文件生成 SRT 字幕文件

positional arguments:
  Media                 可一次识别多个文件

optional arguments:
  -h, --help            show this help message and exit
  --version             show program's version number and exit
  -l 语言, --language 语言  使用什么引擎，默认是配置文件中的第一个 (default: )
```

## 🔋 打赏

本软件完全开源，用爱发电，如果你愿意，可以以打赏的方式为我充电：

![sponsor](assets/Sponsor.png)

## 😀 交流

如果有软件方面的反馈可以提交 issues，或者加入 [QQ 群：1146626791](https://qm.qq.com/cgi-bin/qm/qr?k=DgiFh5cclAElnELH4mOxqWUBxReyEVpm&jump_from=webapi) 