# 上传到 GitHub 的步骤（你执行 / 给我授权我执行）

> 档案夹：`~/hermes_projects/twse_analysis_2026_06_16_github/`
> 内容：台股 20 大事件驱动分析包（详见 `README.md`）
> 状况：本地已就绪，**未**初始化 git、**未**登入 GitHub。

## 0) 你需要先登入（一次性）

> 你说「我有 GitHub 账号」— 那就登入一下。我不会主动 `gh auth login`（那个会开浏览器要你打码），所以**这一步请你自己跑**：

```bash
gh auth login
# 选 GitHub.com → HTTPS → Login with a web browser（推荐）
# 跟着浏览器步骤走完即可
```

登入后确认：

```bash
gh auth status
# 应该看到 "Logged in to github.com as <你的账号> (oauth_token)"
```

## 1) 在 GitHub 网页上建一个空仓库

去 https://github.com/new 建一个空仓库，例如：

- Repository name: `twse-top20-event-analysis-2026-06`
- Description: `台股 20 档近 10 日涨幅 Top 10 事件驱动分析 (2026-06-16 收盘)`
- Public（公开才能分享）
- **不要**勾 Add a README / .gitignore / license（我们本地已有）

记录仓库 URL，例如：`https://github.com/<你的账号>/twse-top20-event-analysis-2026-06.git`

## 2) 初始化本地 git 并推送（你执行 / 或明确告诉我「执行」我就跑）

```bash
cd ~/hermes_projects/twse_analysis_2026_06_16_github

git init -b main
git add .
git status               # 检查 .gitignore 是否把 .DS_Store / *.pkl 排除
git commit -m "台股 20 大近 10 日涨幅 Top 10 事件驱动分析 (2026-06-16 收盘)"
git remote add origin https://github.com/<你的账号>/twse-top20-event-analysis-2026-06.git
git push -u origin main
```

## 3) 我可以代跑吗？

可以，但**你必须**先做完第 0 步（`gh auth login`）并在下一句明确说：

> 「**用 gh 推到 <你的仓库 URL>**」

我会执行：

```bash
cd ~/hermes_projects/twse_analysis_2026_06_16_github
git init -b main && git add . && git commit -m "..." && \
  git remote add origin <URL> && git push -u origin main
```

并在最后给你贴**实际输出**（commit SHA、push 的 remote URL），**不**伪造结果。

## 4) 不想用 gh？也可以用 PAT

```bash
git remote add origin https://<TOKEN>@github.com/<你的账号>/<repo>.git
git push -u origin main
```

> **不建议**把 PAT 写进 shell history；建议用 `gh auth login` 的方式，token 由 gh 安全保管。

## 5) 想让我现在就跑哪几步？

请明确告诉我（任选其一）：

- A. 「**用 gh 推到 <URL>**」 — 完整跑 1+2 步
- B. 「**只跑 git init + commit**，push 等我」 — 跑 1 步，push 你自己来
- C. 「**先别动**」 — 我等你把 gh auth login 跟仓库 URL 给我
