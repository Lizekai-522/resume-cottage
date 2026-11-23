# 简历小屋

这是一个可在本地运行的静态 3D 简历网站。项目自带 Three.js 依赖和默认配乐，无需安装 npm 包，启动后可以离线访问。

## 启动

- **Windows**：解压整个源码包，双击 `start-local.cmd`，在浏览器打开 `http://127.0.0.1:8000`。本机需要安装 Node.js 或 Python 3。
- **命令行**：在解压目录运行 `node server.mjs`。如端口已被占用，可运行 `node server.mjs 8001`，再打开对应端口。
- **Python 3**：也可以运行 `python -m http.server 8000 --bind 127.0.0.1 --directory dist`。
- 部署到自己的静态网站时，上传整个 `dist` 目录中的内容。请通过 HTTP 或 HTTPS 打开，浏览器直接打开 HTML 文件时通常会阻止加载 JavaScript 模块。

## 布置与修改内容

进屋后点击「布置房间」。可以应用「阅读会客角」或「卧室起居」方案，也可以点击家具库添加单件家具，再在画面里拖动。桌面端还支持把家具直接从库里拖进场景。选中物件后可旋转，刚摆放的家具可以移除，也可以撤销上一步或还原初始布置。

自我介绍在屋外邮箱。简历内容、布局和自选曲目保存在当前浏览器。网页的「导出备份」包含介绍、简历内容和布局，自选曲目请保留原始音频文件。

## 文件结构

- `dist/index.html`：界面、镜头和交互流程。
- `dist/cottage.js`、`dist/room.js`：屋外和室内的 3D 模型。
- `dist/furniture.js`、`dist/room-layout.js`：家具库、拖放、布置方案和存档。
- `dist/surface-pages.js`：物件表面的文字和图片。
- `dist/themes.js`、`dist/easter-eggs.js`、`dist/night-sky.js`：风格匹配、彩蛋和星空。
- `dist/music.js`、`dist/entry-music.mp3`：玄关唱机和默认配乐。
- `dist/vendor/`：Three.js 0.160.0 及其许可证。
