# Changelog

All notable changes to BookmarkSync are documented here.

## [1.1.2] — 2026-06-22

Chrome Web Store resubmission after **Code Readability** rejection (obfuscated JS in store ZIP).

### Fixed
- Chrome / Web Store builds use **minification only** (`WXT_SKIP_OBFUSCATION=1`); `javascript-obfuscator` is no longer applied to packages submitted to Chrome.
- `scripts/check-store-zip.mjs` fails the build if `_0x…` obfuscator identifiers remain in the Chrome bundle.
- **`docs/PRIVACY.md`** — English/Chinese aligned with v1.1.2 (S3, E2E, tabs/windows/webNavigation, tab sessions, broken-link check).

## [1.1.1] — 2026-06-20

Chrome Web Store release following **1.1.0**.

### Added
- Header version badge on options / popup UI.
- Incremental bookmark sync (no full clear-and-rewrite on merge/download).
- Remote snapshots stored under `BookmarkSync/_snapshots/` (not repo root).
- Configurable remote snapshot retention (max count, max age, scheduled cleanup).

### Improved
- Sync UI no longer blocks the whole panel while syncing; other tabs stay usable.
- Sync mutex prevents parallel merge/upload/download races.
- Local/remote counts align after merge; URL normalization unified.
- 自动同步：各提供方独立注册周期 alarm；变更模式支持间隔设置与节流；S3 配置变更会触发 alarm 重建。
- 书签数量：本地/远端统一按同步范围（scope）统计，手动同步后两侧计数一致。
- 配置备份说明缩短为两行以内。
- **Mac 应用**：与扩展对齐（`SyncCounts.swift`、`AutoSyncService`、设置 UI、远程快照子目录与保留策略）。

### Fixed
- Double-click sync could inflate bookmark counts and freeze the UI.
- 合并后本地/远端书签计数不一致（按唯一 URL 计数）。

## [1.1.0] — 2026-06-19

### Added

- **Tools hub** — Health overview, duplicate bookmark detection & cleanup, broken-link checker, empty-folder cleanup, organize by domain, HTML/JSON import & export
- **Remote snapshot center** — List remote snapshots, preview diff, restore from snapshot (GitHub / Gitea / WebDAV / S3)
- **Merge preview** — See local-only / remote-only items before merge sync
- **Version history** — Browse Git commits (GitHub / Gitea) or remote snapshot history with diff preview
- **Config backup** — Export/import settings profiles; local config backup list
- **S3-compatible storage** — Full UI for endpoint, bucket, keys, auto-sync, and notifications
- **Advanced sync** — Delete protection, read-only mirror mode, sync scope, folder exclude patterns, E2E encryption UI & remote re-encrypt
- **Scheduled tool tasks** — Optional periodic duplicate / link checks (Tools)
- **Tab sessions 2.0** — Save, restore, and sync named tab sessions
- **Production build hardening** — Minification, no source maps, optional JS obfuscation for release ZIPs
- **Chrome Web Store publish scripts** — `npm run publish:chrome`, local OAuth token flow

### Improved

- Tools panel reorganized into Health, Backup, Governance, Session, Platform groups
- Duplicate detection 2.0 — URL normalization (tracking params, www)
- Link checker 2.0 — Strictness levels, inconclusive handling, batch remove
- i18n — Extended `en` / `zh_CN` strings for all new tools
- macOS app parity (separate deliverable) — Tools tab, S3/E2E, merge preview, version history

### Fixed

- Sync guards — Delete protection blocks destructive download when local bookmarks exist
- Read-only mode blocks remote uploads consistently
