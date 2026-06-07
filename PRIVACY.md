# BookmarkSync Privacy Policy

**Last updated:** June 7, 2026

BookmarkSync ("the Extension" or "the App") helps you sync browser bookmarks with storage you control: **GitHub Gist**, your own **Gitea** server, or a **WebDAV** folder. This policy describes what data is handled and how it is used.

## Summary

- BookmarkSync **does not operate developer-owned servers** for sync.
- Your bookmarks and credentials stay **on your device** and in **storage you configure**.
- We do **not** sell, rent, or share your data with third parties for advertising or analytics.

## Data the Extension Handles

### Browser bookmarks

The Extension (or macOS App) reads and modifies bookmarks to upload, download, merge, restore, or clear them when **you** trigger those actions or when auto-sync is enabled.

### Sync configuration

Settings such as sync provider (GitHub / Gitea / WebDAV), Gist ID, Gitea URL, WebDAV folder URL, file names, auto-sync mode, and notification preferences are stored locally (`chrome.storage.sync` / `chrome.storage.local`, macOS UserDefaults, or iCloud config backup if you enable it).

### Credentials

If you provide credentials, they are stored on your device only:

- GitHub Personal Access Token  
- Gitea access token  
- WebDAV username and password (Basic authentication)

These are used only to access **your** configured remote storage. They are **not** transmitted to BookmarkSync developers.

### Local snapshots and logs

Bookmark snapshots, configuration backups, and sync logs may be stored locally to support restore and troubleshooting. They are not uploaded unless you sync bookmarks to your remote storage.

## Where Data Is Sent

When you sync, bookmark data and related JSON files are sent only to:

- **GitHub** (`github.com`, `githubusercontent.com`) — when you configure GitHub Gist sync  
- **Your Gitea server** — only the origin you configure; browser extension requests permission at runtime  
- **Your WebDAV server** — only the origin/folder URL you configure; browser extension requests permission at runtime  

No bookmark or credential data is sent to the BookmarkSync author or any intermediary service operated for BookmarkSync.

## Permissions (Browser Extension)

| Permission | Purpose |
|------------|---------|
| `bookmarks` | Read/write bookmarks for user-initiated sync |
| `storage` | Save settings, snapshots, logs, and backups locally |
| `alarms` | Run scheduled auto-sync when enabled |
| `notifications` | Optional sync status notifications |
| GitHub host access | Access your configured Gist |
| Optional `*://*/*` | Requested at runtime when you configure a **private Gitea URL** or **WebDAV URL** and test/sync |

## macOS App

The macOS companion app reads Safari bookmarks via `Bookmarks.plist` when you grant **Full Disk Access** or select the bookmarks file. Synced data goes only to remotes you configure (GitHub / Gitea / WebDAV), same as the browser extension.

## Data Retention and Deletion

- **Uninstall the extension or app** — removes locally stored data (subject to OS/browser behavior).  
- **Clear remote data** — use in-app actions or delete files on GitHub / Gitea / WebDAV directly.  
- **Revoke credentials** — delete or rotate tokens/passwords on GitHub, Gitea, or your WebDAV account at any time.

## Children

BookmarkSync is not directed at children under 13, and we do not knowingly collect personal information from children.

## Changes

We may update this policy when the product changes. The "Last updated" date at the top will reflect the latest revision.

## Contact

For privacy questions, open an issue in the project repository or contact the publisher listed on the Chrome Web Store / Firefox Add-ons listing.

---

# BookmarkSync 隐私政策（中文）

**最后更新：** 2026 年 6 月 7 日

BookmarkSync（「本扩展」或「本应用」）帮助您将浏览器书签同步到您自行控制的存储：**GitHub Gist**、**私有 Gitea** 或 **WebDAV 目录**。本政策说明处理哪些数据及如何使用。

## 概要

- 书签同步**不经过开发者服务器**。
- 书签与凭据保存在**您的设备**及**您配置的远程存储**中。
- **不会**为广告或分析目的出售、出租或共享您的数据。

## 处理的数据

### 浏览器书签

仅在您手动操作或开启自动同步时，读取或修改书签（上传、下载、合并、恢复、清空）。

### 同步配置

同步方式、Gist ID、Gitea 地址、WebDAV 目录地址、文件名、自动同步模式、通知开关等，保存在浏览器扩展存储、macOS 本地设置，或您开启的 iCloud 配置备份中。

### 凭据

以下凭据**仅保存在本机**，用于访问您配置的远程存储，**不会**发送给 BookmarkSync 开发者：

- GitHub Personal Access Token  
- Gitea Token  
- WebDAV 用户名与密码（Basic 认证）

### 本地快照与日志

可能在本地保存书签快照、配置备份和同步日志，用于恢复与排查；除非您主动同步，否则不会上传至第三方。

## 数据去向

同步时，数据仅发送至：

- **GitHub**（配置 Gist 同步时）  
- **您指定的 Gitea 服务器**（扩展在运行时按您配置的域名申请权限）  
- **您指定的 WebDAV 服务器**（扩展在运行时按您配置的域名申请权限）  

不向 BookmarkSync 作者或任何中间服务传输书签或凭据。

## 权限说明（浏览器扩展）

| 权限 | 用途 |
|------|------|
| `bookmarks` | 用户发起的同步时读写书签 |
| `storage` | 本地保存设置、快照、日志、备份 |
| `alarms` | 启用定时自动同步 |
| `notifications` | 可选的同步结果通知 |
| GitHub 主机访问 | 访问您配置的 Gist |
| 可选 `*://*/*` | 配置 **Gitea** 或 **WebDAV** 地址并测试/同步时，按该域名运行时申请 |

## macOS 应用

macOS 伴侣应用在您授予**完全磁盘访问**或手动选择书签文件后，读取 Safari 书签；远程同步目标与扩展相同（GitHub / Gitea / WebDAV），数据同样只发往您配置的存储。

## 删除数据

- **卸载扩展或应用** — 清除本地数据（以系统/浏览器行为为准）  
- **清空远程** — 使用应用内功能，或在 GitHub / Gitea / WebDAV 上直接删除对应文件  
- **撤销凭据** — 在 GitHub、Gitea 或 WebDAV 账户中随时修改或删除密码/Token  

## 联系我们

如有隐私相关问题，请在项目仓库提交 Issue，或通过 Chrome 网上应用店 / Firefox 附加组件 listing 中的发布者信息联系。
