# B 站直播间弹幕自动发送

**中文** | [English](README_EN.md)

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.1-brightgreen.svg)](src/main.ts)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6.svg?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![UserScript](https://img.shields.io/badge/UserScript-Tampermonkey%20%7C%20Violentmonkey-ff6a00.svg)](https://www.tampermonkey.net/)
[![Platform](https://img.shields.io/badge/platform-live.bilibili.com-FB7299.svg?logo=bilibili&logoColor=white)](https://live.bilibili.com/)

一个用于 B 站直播间的油猴脚本，可以按设定间隔自动轮播发送弹幕，并提供可拖拽的控制面板。

## 功能特性

- 自动向 B 站直播间发送弹幕
- 支持多条弹幕循环轮播（使用 `;` 分隔）
- 可拖拽的控制面板，位置自由摆放
- 支持自定义发送间隔
- 实时显示已发送次数
- 一键开始 / 停止发送

## 安装

### 前置条件

安装以下任一油猴扩展：

- [Tampermonkey](https://www.tampermonkey.net/)
- [Violentmonkey](https://violentmonkey.github.io/)

### 从源码构建

```bash
# 1. 克隆仓库
git clone https://github.com/jiejiebiezheyang/b-send-dan.git
cd b-send-dan

# 2. 安装依赖
npm install

# 3. 构建脚本
npm run build
```

构建完成后，将 `dist/main.js` 的内容复制到油猴插件中，新建脚本并粘贴保存即可。

## 使用方法

1. 打开任意 B 站直播间页面（如 [https://live.bilibili.com/](https://live.bilibili.com/)）
2. 脚本自动加载，页面左上角会出现控制面板
3. 在输入框中填写弹幕内容，多条弹幕用 `;` 分隔
4. 点击「发送」开始自动发送，按钮会变为「停止」
5. 再次点击「停止」即可结束发送

## 配置说明

| 配置项   | 说明                                                                                                              |
| -------- | ----------------------------------------------------------------------------------------------------------------- |
| 发送内容 | 多条弹幕用 `;` 分隔，例如 `1;2;3;4;5`                                                                             |
| 发送间隔 | 默认 `3500` 毫秒（3.5 秒），可在 [main.ts](file:///d:/project/cyan/b-send-dan/src/main.ts) 中修改 `interval` 变量 |
| 面板位置 | 按住标题栏拖动即可移动面板                                                                                        |

## 开发

### 项目结构

```
b-send-dan/
├── src/
│   └── main.ts          # 源代码
├── dist/
│   └── main.js          # 编译后的脚本
├── obfuscate.config.json # 混淆配置
├── package.json
├── tsconfig.json
└── README.md
```

### 可用命令

```bash
npm run build      # 构建项目
npm run watch      # 监听模式构建
npm run start      # 运行编译后的代码
npm run obfuscate  # 构建并混淆输出到 dist/obf
npm run clean      # 清理构建产物
```

## 技术栈

- TypeScript
- UserScript（油猴脚本）

## 注意事项

- 请合理使用，避免频繁发送弹幕影响他人观看体验
- 使用前请确保已登录 B 站账号
- 脚本仅在 B 站直播间页面生效

## 许可证

本项目基于 [MIT License](LICENSE) 开源。

## 作者

[jiejiebiezheyang](https://github.com/jiejiebiezheyang)

## 免责声明

本脚本仅供学习和研究使用。使用者需自行承担使用本脚本所产生的一切风险和责任，作者不对因使用本脚本而导致的任何损失、损害或后果承担责任。使用本脚本即表示您同意自行承担所有风险，并遵守 B 站的相关服务条款和社区规范。如因使用本脚本导致账号被封禁、受到处罚或其他任何不良后果，作者概不负责。请合理、合规使用本脚本，尊重他人，共同维护良好的网络环境。
