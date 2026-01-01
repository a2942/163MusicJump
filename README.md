# 🎵 163MusicJump 

> 一个精致、智能的网易云音乐协议跳转与分享工具。

[![Status](https://img.shields.io/badge/Status-Perfect-brightgreen)]() 
[![Author](https://img.shields.io/badge/Author-a2942-red)]()
[![Collaboration](https://img.shields.io/badge/With-Gemini-blue)]()

## ✨ 项目简介

**163MusicJump** 是为了解决网易云音乐在不同平台间跳转不统一、PC端协议不自动播放等痛点而诞生的。它不仅是一个跳转工具，更是一个注重 UI/UX 体验的艺术小品。

通过它，你可以轻松生成一个带有歌曲预览的分享链接，并实现“App优先，网页回退”的智能跳转逻辑。

## 🚀 核心功能

- **智能协议解析**：
  - **手机端**：自动唤起 `orpheus://` 移动端协议。
  - **PC 端**：通过 **Base64 JSON 编码** 封装指令，解决 PC 端只能打开 App 无法自动播放的问题。
- **预览集成**：自动加载网易云官方 Iframe 播放器，跳转前先行预览封面与歌曲信息。
- **优雅的跳转回退**：采用“心跳检测”机制，若用户未安装客户端，2.5秒后自动重定向至网页版，避免页面卡死。
- **自定义询问弹窗**：摒弃了原生丑陋的 `confirm`，使用纯 CSS 打造的毛玻璃质感动效弹窗。
- **便捷分享**：一键生成带 `?id=xxx` 参数的链接，方便分发。

## 🛠 如何使用

1. **直接访问**：在输入框输入歌曲 ID，点击播放或生成链接。
2. **URL 传参**：
   - 格式：`index.html?id=歌曲ID`
   - 示例：<a target="_blank" href="https://a2942.github.io/163MusicJump/?id=2619303313">https://a2942.github.io/163MusicJump/?id=2619303313</a>
   - 效果：页面加载后会自动展示歌曲预览并弹出跳转确认。

## 🎨 界面展示

<img width="697" height="460" alt="image" src="https://github.com/user-attachments/assets/d1b27922-3338-42b2-acb7-12ec675fa979" />


## 🛠 技术细节

- **语言**：原生 HTML5 / CSS3 / JavaScript (ES6+)。
- **动效**：使用 CSS 贝塞尔曲线 (`cubic-bezier`) 实现丝滑的弹窗与滑动效果。
- **逻辑**：监听 `visibilitychange` 与 `blur` 事件，配合时间差计算逻辑判定 App 唤起状态。

## 💖 致谢

本项目由 **a2942** 发起创意与审美把控，由 **Gemini (AI Assistant)** 提供算法实现与逻辑优化。

---

*Crafted with 💖 by Gemini 3 Flash Preview and a2942*
