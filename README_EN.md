# Bilibili Live Danmaku Auto Sender

[中文](README.md) | **English**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.1-brightgreen.svg)](src/main.ts)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6.svg?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![UserScript](https://img.shields.io/badge/UserScript-Tampermonkey%20%7C%20Violentmonkey-ff6a00.svg)](https://www.tampermonkey.net/)
[![Platform](https://img.shields.io/badge/platform-live.bilibili.com-FB7299.svg?logo=bilibili&logoColor=white)](https://live.bilibili.com/)

A UserScript for Bilibili live rooms that automatically sends danmaku on a fixed interval, with a draggable control panel.

## Features

- Automatically sends danmaku to Bilibili live rooms
- Rotates through multiple messages (separated by `;`)
- Draggable control panel that can be placed anywhere
- Configurable sending interval
- Live counter of sent messages
- One-click start / stop

## Installation

### Prerequisites

Install one of the following userscript managers:

- [Tampermonkey](https://www.tampermonkey.net/)
- [Violentmonkey](https://violentmonkey.github.io/)

### Build from source

```bash
# 1. Clone the repository
git clone https://github.com/jiejiebiezheyang/b-send-dan.git
cd b-send-dan

# 2. Install dependencies
npm install

# 3. Build the script
npm run build
```

After building, copy the contents of `dist/main.js` into a new script in your userscript manager and save it.

## Usage

1. Open any Bilibili live room (e.g. [https://live.bilibili.com/](https://live.bilibili.com/))
2. The script loads automatically and a control panel appears in the top-left corner
3. Enter your danmaku text in the input box, separating multiple messages with `;`
4. Click **Send** to start; the button changes to **Stop**
5. Click **Stop** again to end sending

## Configuration

| Option         | Description                                                                                                                |
| -------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Content        | Separate multiple messages with `;`, e.g. `1;2;3;4;5`                                                                      |
| Interval       | Defaults to `3500` ms (3.5 s); change the `interval` variable in [main.ts](file:///d:/project/cyan/b-send-dan/src/main.ts) |
| Panel position | Drag the title bar to move the panel                                                                                       |

## Development

### Project structure

```
b-send-dan/
├── src/
│   └── main.ts          # Source code
├── dist/
│   └── main.js          # Compiled script
├── obfuscate.config.json # Obfuscation config
├── package.json
├── tsconfig.json
└── README.md
```

### Available commands

```bash
npm run build      # Build the project
npm run watch      # Build in watch mode
npm run start      # Run the compiled code
npm run obfuscate  # Build and obfuscate into dist/obf
npm run clean      # Clean build artifacts
```

## Tech Stack

- TypeScript
- UserScript

## Notes

- Please use responsibly and avoid spamming, which degrades the viewing experience for others
- Make sure you are logged into your Bilibili account
- The script only works on Bilibili live room pages

## License

This project is licensed under the [MIT License](LICENSE).

## Author

[jiejiebiezheyang](https://github.com/jiejiebiezheyang)

## Disclaimer

This script is intended for learning and research purposes only. Users assume all risks and responsibilities arising from its use, and the author is not liable for any loss, damage, or consequence caused by using this script. By using this script, you agree to bear all risks yourself and to comply with Bilibili's terms of service and community guidelines. The author takes no responsibility for any account ban, penalty, or other negative outcome resulting from the use of this script. Please use it reasonably and lawfully, respect others, and help keep the community healthy.
