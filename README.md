# UNA · 全球历史（本地点播）

公开站点：https://vincent-karina.github.io/global-history/

## 怎么看
1. 在线打开 https://vincent-karina.github.io/global-history/ 。
2. 本地打开本目录下的 `index.html`（双击即可，`file://` 可用）。
3. 点「播放」进入单课页；视频优先加载 `全球历史-第N课/video-lite.mp4`。
4. 也可直接进入各课文件夹，打开讲义 HTML 或完整 `video.mp4`。

## 目录结构
```
全球历史/
  index.html
  README.md
  deploy-notes.md
  lessons/第N课.html
  全球历史-第N课/
    video-lite.mp4   # 点播用（约 720p）
    video.mp4        # 完整版（若有）
    *.html           # 讲义
```

## 课表
- 第一周（人类起源与农业革命）：第1–7课
- 第二周（早期城市、国家与文字）：第8–14课
- 第三周（青铜时代的帝国与网络）：第15课起

## 在线发布
GitHub Pages 从分支 `main`、目录 `/`（仓库根）发布。

- 公开地址：https://vincent-karina.github.io/global-history/
- 本地预览：打开仓库根目录的 `index.html`

推送后 Pages 可能需要一两分钟才可访问。第 9–15 课的 `video-lite.mp4` 尚未全部放入；第 1–4 课按设计没有视频。部署细节见 `deploy-notes.md`。
