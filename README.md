# AI 网关（Cuckoo Code 插件）

把 Cuckoo 的 AI 网页版暴露成 **OpenAI 兼容 API**，让局域网设备（手机 / LobeChat / 任何支持 OpenAI 的客户端）直接调用。附管理网站（Key 管理 / 请求日志）。

## 安装

在 Cuckoo Code 的「插件市场」搜索 **AI 网关**，一键安装。

或手动：
```bash
# 把本仓库内容放到 ~/.cuckoo/plugins/ai-gateway/
```

## 客户端配置

```
Base URL:  http://<本机局域网IP>:18900/v1
API Key:   （管理网站里创建的 sk-cuckoo-...）
Model:     cuckoo-default
```

## 功能

- **OpenAI 兼容 API**：`/v1/chat/completions`（流式 + 非流式）、`/v1/models`
- **独立隐藏窗口**：每次请求开一个隐藏窗口，工具循环天然正常，不污染你的对话
- **流式思考**：思考 → `reasoning_content`，正文 → `content`（像真 API）
- **管理网站**：Key 管理、请求日志、启停开关
- **侧边栏面板**：一键查看地址、开关网关、整活模式

## 安全

- 默认绑定 `0.0.0.0`（局域网可访问）——想只本机用，把 host 改成 `127.0.0.1`
- 管理密码默认 `admin`，**建议改掉**
- 可要求 API Key（默认开）

## 许可证

MIT
