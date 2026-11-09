# 在线站部署说明

## 当前状态
- 仓库：`Vincent-Karina/global-history`（公开），站点已推到 `main`
- 预期 Pages 地址：https://vincent-karina.github.io/global-history/
- 本地预览：打开仓库根目录的 `index.html`
- 已放入的 lite 视频：第 5–8 课。第 9–15 课待补；第 1–4 课无视频（设计如此）。
- Pages **尚未开启**。`POST /repos/Vincent-Karina/global-history/pages` 返回 403（`Resource not accessible by integration`）。该接口需要 GitHub App 的 `administration:write` 与 `pages:write`；当前 cloud agent 令牌没有 Administration 权限，Actions 的 `GITHUB_TOKEN` 也不能创建 Pages 站点。
- 管理员打开方式：Settings → Pages → Build and deployment → Deploy from a branch → Branch `main`、Folder `/ (root)` → Save。生效约 1–2 分钟。可用 `gh api repos/Vincent-Karina/global-history --jq .has_pages` 确认为 `true`。

## 建议
- GitHub 账号：`Vincent-Karina`
- 公开仓库名：`global-history`
- Pages 地址：`https://vincent-karina.github.io/global-history/`

## 待推文件（站点包根目录）
来源：`/workspace/全球历史-site/`（与桌面门户同结构）

必推：
- `index.html`
- `README.md`
- `deploy-notes.md`
- `lessons/第1课.html` … `lessons/第15课.html`
- 各课目录内 **仅** `video-lite.mp4` + 讲义 `*.html`（不要推完整 `video.mp4`、clips、源素材）

## lite 视频清单与大小
仓库里目前的网页压缩版（均 < 15 MB，未使用 Git LFS）：
- `全球历史-第5课/video-lite.mp4` — 8.7 MB
- `全球历史-第6课/video-lite.mp4` — 8.4 MB
- `全球历史-第7课/video-lite.mp4` — 12 MB
- `全球历史-第8课/video-lite.mp4` — 7.6 MB

第 9–15 课的 `video-lite.mp4` 尚未放入。

## 缺失
- 第1–4课：无标准有声片（按设计不放 video-lite）
- 第9–15课：播放页与讲义已在，`video-lite.mp4` 待后续提交

## 推送步骤（给父代理 / Vincent）
1. 在 GitHub 新建空仓库 `global-history`（Public）。
2. 将本站点包内容推到 `main`（可用 cloud agent / 本机 git）。
3. Settings → Pages → Deploy from branch `main` / root。
4. 等待 Pages 生效（约 1–2 分钟）后把真实 URL 告知用户。

站点内容已在 `main`。Pages 源应按上面的设置选 `main` / `/`。第 9–15 课视频到达后再追加对应的 `video-lite.mp4` 即可，不必改 Pages 设置。
