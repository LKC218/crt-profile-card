# LKC218 Profile

GitHub 个人自述页仓库。CRT 动态名片见 `assets/crt-card.svg`。

## 结构

```
README.md           # Profile 首页（GitHub 自动读取）
assets/crt-card.svg # 无脚本 CRT 打字机动画名片
```

## 更新名片

1. 改 `assets/crt-card.svg` 文案（`whoami` / `slogan` 各行）
2. 本地用浏览器打开 SVG 预览动画
3. 提交并 push 到 `main`

## 发布到 GitHub

Profile README 要求仓库名与用户名一致：`LKC218/LKC218`。

```bash
# 若本机 gh 已登录
gh repo create LKC218/LKC218 --public --source=. --push
```

或在网页新建空仓库 `LKC218/LKC218` 后：

```bash
git remote add origin git@github.com:LKC218/LKC218.git
git push -u origin main
```
