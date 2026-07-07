# BookmarkSync v1.1.10 — Release notes

## English

v1.1.9

FIXED: Sync errors showed only a generic message — real cause (token, WebDAV HTTP, E2E passphrase, etc.) now appears in the alert
FIXED: Merge sync false "incomplete local write" when duplicate URLs exist in different folders (e.g. 583/584)
IMPROVED: Backup policy split into 4 options (settings / local snapshot / remote archive / manual sync) with weekly mode; remote archive defaults to once per week

## 中文

v1.1.9

修复：同步失败只显示「错误」— 现显示具体原因（Token、WebDAV、加密口令等）
修复：合并同步误报本地写入不完整（同一链接多文件夹时如 583/584）
改进：备份策略拆为 4 项可独立配置，新增每周；远程归档默认每周一次
