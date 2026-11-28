# 开发日志

GitHub Pages 从 `main` 的根目录发布。站点读取 `posts.json`，按日期从新到旧显示，同一天按清单中的顺序显示。

## 发布一篇

1. 在 `posts.json` 的数组开头新增一项。填 `date`（以原始工作会话的北京时间为准，格式 `YYYY-MM-DD`）、`title`、`text`（1–3 句纯文本）。
2. 有配图或短片时，将可公开的副本放到 `media/<短名>/<文件名>`。目录名和文件基本名用小写字母、数字、连字符或下划线。可用 PNG、JPEG、WebP、AVIF、GIF、MP4 或 WebM。为文章填一个 `media` 对象，含 `type`（`image` 或 `video`）、`src`（仓库相对路径）和 `alt`（图片替代文本或短片说明）。检查权限、画面和声音里是否包含私有信息。各段需要独立配图时，用空行分隔 `text` 中的段落，将 `media` 写成按段落顺序排列的数组。纯文字段可填 `null`。
3. 在仓库根目录运行 `python3 -m http.server 8000`，打开 `http://localhost:8000/` 预览。检查最新文章位置、窄屏排版、文字和媒体播放。
4. 把文章与媒体一起提交到 `main` 并推送。等 Actions 里的 Pages 部署成功后，打开公开站点验证文章和媒体。

公开站点：https://junhaoli95.github.io/devlog/
