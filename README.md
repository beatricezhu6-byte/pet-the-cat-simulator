# 撸猫模拟器

中文版单文件交互式撸猫网页。13 只猫，支持抚摸、拉尾巴、Web Audio 合成呼噜声、体格调节和夜间模式。

[Live Demo](https://pet-cat-sim.app.workbuddy.host/?sharecode=SLVSO2KW2E) · [下载 index.html](index.html)

## Features

- 13 只猫，不同花色与互动反应
- 抚摸触发呼噜声（Web Audio API 实时合成，无音频文件）
- 可拖动拉长尾巴，松手回弹
- 滑块调节猫的体格
- 夜间模式切换
- 全部资源内嵌，零外部依赖，离线可用

## Quick Start

直接双击 `index.html`，或：

```bash
git clone https://github.com/beatricezhu6-byte/pet-the-cat-simulator.git
cd pet-the-cat-simulator
# 用浏览器打开 index.html
```

不需要 Node、不需要构建、不需要服务器。

## Project Structure

```
.
├── index.html       # 成品：HTML/CSS/JS/贴图全部内嵌，838 KB
├── app.js           # 交互逻辑（可读源码）
├── layout.html      # 界面与样式（可读源码）
├── directory.json   # 贴图索引
└── photos.bin       # AVIF 贴图数据
```

`index.html` 是自包含产物；其余四个文件是还原出的可读源码，便于二次开发。

## Tech Stack

- 原生 HTML / CSS / JavaScript，无框架、无依赖
- Web Audio API 合成呼噜声
- 贴图使用 AVIF 编码，打包为二进制 `photos.bin`，运行时索引加载

## Development

| 要改什么 | 改哪个文件 |
| --- | --- |
| 文案、布局、样式 | `layout.html` |
| 交互逻辑 | `app.js` |
| 猫的贴图 | `photos.bin` + `directory.json` |

改完源码后，按 `index.html` 中的内嵌方式重新注入四个文件即可生成新成品。
