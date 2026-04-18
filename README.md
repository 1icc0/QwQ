# QwQ

一个现代化、轻量级的QQ机器人Web端聊天界面，基于NapCat WebSocket协议构建。

<p align="center">
  <img src="https://img.shields.io/badge/license-GPL_v2-blue.svg" alt="License">
  <img src="https://img.shields.io/badge/built_with-HTML/CSS/JS-007396?style=flat&logo=javascript" alt="Built With">
</p>


## ⚡ 项目概述
QwQ是基于NapCat实现的web端的极其轻量的QQ客户端，通过NapCat提供的api实现在浏览器上查看好友列表、消息、发送消息等，暂不支持发送文件和图片


## 🎯 快速开始

### 前置条件

1. 已安装并运行NapCat服务。
2. 确保NapCat的WebSocket服务器已启用。

### 使用步骤

1. **获取QwQ**
    - 您可以直接下载 `index.html` 文件，或用任何HTTP服务器托管它。

2. **启动**
    - 在浏览器中打开 `index.html`。

3. **连接NapCat**
    - 填入NapCat的WebSocket地址（例如：`ws://127.0.0.1:3001`）和可选的Access Token。
    - 点击“连接”按钮。

4. **开始聊天**
    - 连接成功后，左侧面板会加载您的好友和群组列表。
    - 点击任一联系人或群组，即可在右侧主区域开始聊天。

### NapCat配置

1. **安装**
    - 网上教程很多，这里不再过多赘述。

2. **添加Websockets服务端**
    - Host: 0.0.0.0
    - Port: 随意，这个端口与后面进入QwQ中要填的端口相同

## 📱 界面预览

界面主要分为三个区域：

1.  **左侧边栏**：提供核心功能切换（消息、联系人、群组、设置）。
2.  **联系人/群组列表**：展示所有好友和群组，包含最后一条消息预览、时间和未读计数。
3.  **主聊天区域**：显示完整的对话历史、消息发送者头像/名称、时间，以及底部的消息输入框和发送按钮。


## 🔧 技术栈

- **前端**：纯原生HTML5、CSS3、JavaScript (ES6+)
- **通信协议**：WebSocket (通过NapCat与QQ客户端通信)
- **样式**：自定义CSS变量实现主题化，Flexbox/Grid布局
- **数据持久化**：`localStorage` 保存连接配置

## 🤝 与NapCat的API交互

QwQ 通过调用NapCat的标准API来实现功能，主要调用包括：

- `get_login_info`: 获取登录机器人自身信息。
- `get_friend_list` / `get_group_list`: 获取好友和群组列表。
- `send_private_msg` / `send_group_msg`: 发送私聊和群聊消息。
- `get_friend_msg_history` / `get_group_msg_history`: 获取聊天记录。

## 📦 部署

QwQ是一个纯静态单页应用，部署极其简单：

1. 将 `index.html` 文件放置在任意Web服务器目录下（如Nginx, Apache, Caddy等）。
2. 通过浏览器访问该文件对应的URL即可。

**注意**：由于浏览器同源策略，如果NapCat服务运行在不同于托管QwQ页面的域名或端口上，NapCat服务端需要配置允许相应的跨域请求（CORS）。


## 🙏 致谢

- 感谢NapCat项目提供了强大稳定的QQ协议实现和WebSocket接口。
- 感谢Claude协助开发了部分代码

## ⚠️ 免责声明

本项目（QwQ）仅为NapCat服务提供了一个可视化的Web聊天界面，是一个**前端客户端**。所有与QQ服
使用QQ机器人应遵守腾讯QQ的相关用户协议与法律法规。开发者不对使用本界面进行任何违规行为负责。
