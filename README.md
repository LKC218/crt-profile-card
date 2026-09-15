# crt-profile-card

GitHub Profile 用的 **无脚本 CRT 动态名片**（SVG + SMIL）：绿屏打字机、扫描线、辉光。

- 资产：`assets/crt-card.svg`（960×300，自包含，无 JS）
- 展示：由 Profile 仓库 [`LKC218/LKC218`](https://github.com/LKC218/LKC218) 通过 raw 链接引用
- 主题：monochrome-green / green-scanlines
- 实现：手写 SVG SMIL，不依赖 typed-crt 源码

## 预览

本地直接打开：

```text
assets/crt-card.svg
```

或用浏览器查看动画。

## 双仓架构

| 仓库 | 职责 |
| --- | --- |
| `LKC218/crt-profile-card` | 源资产 + 维护文档（本仓） |
| `LKC218/LKC218` | GitHub Profile README，引用本仓 raw SVG |

Profile 引用地址：

```text
https://raw.githubusercontent.com/LKC218/crt-profile-card/main/assets/crt-card.svg
```

## 维护

见 [README-维护说明.md](README-维护说明.md)。
