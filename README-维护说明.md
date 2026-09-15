# 维护说明

## 双仓分工

| 仓库 | 本地 | 内容 |
| --- | --- | --- |
| `LKC218/crt-profile-card` | `G:\项目\LKC218-LKC218` | `assets/crt-card.svg`、本说明、项目 README |
| `LKC218/LKC218` | 建议 `G:\项目\profile-LKC218` | 仅 Profile `README.md`，不放 SVG 源文件 |

## 结构

```text
crt-profile-card/
├── README.md              # 项目说明
├── README-维护说明.md
├── .gitignore
└── assets/
    └── crt-card.svg       # 无脚本 CRT 打字机动画名片

LKC218/LKC218/
└── README.md              # Profile 首页（GitHub 自动读取）
```

## 更新名片文案

1. 改 `assets/crt-card.svg` 中 `whoami` / `slogan` 各行
2. 浏览器打开 SVG 预览打字机节奏
3. 提交并 push 到 `crt-profile-card` 的 `main`
4. Profile 页 raw 图会缓存；若未更新可等几分钟，或在 Profile README 加无害 query（如 `?v=2`）强制刷新

## Profile README 模板

`LKC218/LKC218/README.md` 建议内容：

```markdown
<p align="center">
  <img src="https://raw.githubusercontent.com/LKC218/crt-profile-card/main/assets/crt-card.svg" alt="LKC218 CRT 名片" width="720">
</p>

<p align="center">
  <strong>LKC218</strong> · 本地优先的小工具
</p>

<p align="center">
  在做提示词管理、3D 工具链和一些桌面端小软件。<br>
  Building local-first tools.
</p>
```

## 发布

### 1. 项目仓（本目录）

```bash
# 网页建空公开仓：LKC218/crt-profile-card（不要初始化 README）
git remote add origin https://github.com/LKC218/crt-profile-card.git
git push -u origin main
```

### 2. Profile 仓

网页新建空公开仓 `LKC218/LKC218`（不要初始化 README），放入上方模板 README 后 push。

Profile 仓名必须与用户名完全一致，否则不会出现在主页。

## 可选静态兜底

若需 PNG fallback（不支持 SMIL 的场景）：

1. 浏览器打开 SVG，等动画停在完整态
2. 截图导出为 `assets/crt-card-static.png`
3. Profile README 可用 `<picture>` 或说明链到 PNG
