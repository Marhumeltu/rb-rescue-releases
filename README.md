# RB Rescue

**Free your Rekordbox library from old USB file paths.**  
**让 Rekordbox 曲库摆脱旧 U 盘的路径依赖。**

**Unplug an old DJ USB drive and suddenly see a wall of “Missing Files” in Rekordbox?** If tracks were imported directly from that drive years ago, your Collection may still point to its old file paths—even if you've since switched to a local music library.

**拔掉旧 DJ U 盘，Rekordbox 就出现一大片 Missing Files（丢失文件）？** 如果你以前直接从 U 盘导入过音乐，Collection 可能至今仍指向那个旧盘。后来改用电脑本地曲库，这些历史路径就成了麻烦。

**RB Rescue helps you identify and safely copy those still-readable files to a new location, so you can reconnect the original Rekordbox tracks with its official Relocate / Auto Relocate feature.** It is not a replacement for Rekordbox's built-in library backup, and it cannot recover audio that no longer exists.

**RB Rescue 帮你根据现有曲库找到仍依赖旧路径的音频文件，批量检查、分类并安全复制到新位置，然后配合 Rekordbox 官方 Relocate / Auto Relocate 重新关联原来的曲目。** 它不替代 Rekordbox 的曲库备份功能，也不能凭空找回已经丢失的音频文件。

[**Download RB Rescue v0.1.0 / 下载 v0.1.0**](https://github.com/Marhumeltu/rb-rescue-releases/releases/latest) · [English](#english) · [简体中文](#简体中文)

---

## English

### The problem: a library still tied to an old drive

Imagine you've spent years building playlists, hot cues, beatgrids, ratings, and comments in Rekordbox. Some of your tracks were imported straight from a DJ USB drive or an external disk, with locations such as:

`J:\Contents\Artist\Album\Track.mp3`

Now you'd rather keep the music on your computer or a new disk. But copying it manually **doesn't update the file paths in your existing Rekordbox Collection**. Disconnect the old disk, and those tracks become *Missing Files*. Re-importing them as new tracks is not the same as reconnecting the existing records you've already organized.

**RB Rescue is for this specific legacy-path cleanup—not ordinary drive-to-drive copying.**

### Do you actually need RB Rescue?

| Your situation | Better starting point |
| --- | --- |
| Moving an otherwise healthy Rekordbox library to another computer | Try Rekordbox's built-in **Backup Library / Restore Library** workflow |
| Only a few tracks show Missing Files, and you already know their new locations | Try Rekordbox **Relocate / Auto Relocate** directly |
| Many existing tracks still point to an old USB/external drive; you need to identify, organize and copy their audio before reconnecting them | **RB Rescue** can help prepare that migration |
| The original disk is lost, unreadable, or the audio files are gone | **RB Rescue cannot recover the missing audio** |

### How it works

1. **Reconnect the old drive** (if needed). The source audio files must be accessible at the paths RB Rescue reads from the XML.
2. **Export your existing Rekordbox Collection as XML.** Keep a backup of the library first.
3. **Open the XML in RB Rescue**, select the old source location(s) and a new destination folder.
4. **Run Scan / Dry Run.** Review which files are referenced by your Collection, which belong to playlists, which do not, and any missing files, conflicts or space issues.
5. **Copy and verify.** RB Rescue safely copies files while preserving relative folders, and outputs migration results plus an **old-path → new-path mapping**. Optional strict SHA-256 verification is available.
6. **Return to Rekordbox** and use its official **Relocate / Auto Relocate** tools to reconnect the *existing* tracks. Check your playlists, cues, beatgrids, and other library data afterward.

**Important:** RB Rescue does not change track locations inside Rekordbox. The final reconnection is a separate action you perform in Rekordbox; preservation of your existing library associations depends on completing that step correctly.

### What RB Rescue does

- Reads **Rekordbox XML** to identify existing track locations; does not access or edit Rekordbox's private database.
- Lets you choose which source drives or folders to process, rather than blindly copying everything.
- Separates tracks **with playlist membership** from tracks **without any playlist membership** into `Recovered_With_Playlist` and `Recovered_No_Playlist`, keeping relative source folders. It **does not** create one folder per playlist.
- Provides a **Dry Run** with missing-file and destination-conflict checks before any copying.
- Uses a **copy-only** workflow: no source deletion, no intentional overwrites, resumable operations, verification and result reports.
- Offers an **English / Simplified Chinese** interface.

### Download and requirements

1. Download [`RBRescue-v0.1.0-win64.zip`](https://github.com/Marhumeltu/rb-rescue-releases/releases/latest).
2. Extract it to a local folder and launch the included application.
3. Prepare the Rekordbox XML export and an accessible source drive, then follow the steps above.

- **Platform:** Windows 10/11 x64 target. Validated in a **Windows 11 Sandbox** environment; Windows 10 has **not** been independently validated.
- **Prerequisite:** [Microsoft Visual C++ Redistributable (x64)](https://aka.ms/vc14/vc_redist.x64.exe).

### Safety and limits

**Back up your Rekordbox library and audio files before starting.** Source music must still be readable. RB Rescue cannot repair corrupted audio, recover an unavailable drive, guess the whereabouts of already-lost files, or automatically fix Rekordbox's Missing Files entries. Review the Dry Run and the destination before copying, and verify the library after Relocate.

### Third-party licenses and source materials

The application includes applicable third-party license texts, copyright/attribution materials, and LGPL library replacement instructions. A separate [third-party source archive](https://github.com/Marhumeltu/rb-rescue-releases/releases/latest) is available with the release.

The included documents explain known limitations in matching some upstream source and attribution materials to precompiled third-party binaries. This distribution repository does **not** publish RB Rescue's own development source code; third-party license rights remain unaffected.

**Disclaimer:** RB Rescue is an independent project and is not affiliated with, sponsored by, or endorsed by AlphaTheta or Pioneer DJ.

---

## 简体中文

### 这个工具要解决什么问题？

假设你已经用 Rekordbox 整理了很多年的 Playlist、Hot Cue、Beatgrid、评分和备注。但早些年你曾**直接从 DJ U 盘或移动硬盘导入音乐**，Collection 保存的实际路径可能是：

`J:\Contents\Artist\Album\Track.mp3`

后来你改用电脑本地曲库，想把这些旧盘里的音乐也集中搬回来。问题是：**手动复制文件，不会更新 Rekordbox 原有曲目的文件路径。** 一旦拔掉旧 U 盘，曲目就可能显示 Missing Files；而将这些音乐重新 Import 成新曲目，又不等于找回原来那些已经整理过的曲库记录。

**RB Rescue 处理的正是这种历史遗留的路径依赖，而不是一般的硬盘搬家。**

### 什么时候需要 RB Rescue？

| 你的情况 | 更合适的处理方式 |
| --- | --- |
| 正常使用的 Rekordbox 曲库需要整体迁移到另一台电脑 | 优先考虑 Rekordbox 官方 **Backup Library / Restore Library** |
| 只有少量曲目 Missing，且知道文件现在在哪 | 先尝试 Rekordbox 官方 **Relocate / Auto Relocate** |
| 大量旧曲目仍指向 U 盘或移动硬盘，需要批量筛选、复制到本地，再关联回原 Collection | 这正是 **RB Rescue** 的适用场景 |
| 原 U 盘丢失、损坏或音频已经不存在 | **RB Rescue 无法恢复丢失的音频文件** |

### 如何使用？

1. **接入旧 U 盘或硬盘。** 确保源音乐仍可从 XML 指向的位置正常读取。
2. **从现有 Rekordbox 曲库导出 XML。** 操作前先备份曲库。
3. **在 RB Rescue 中打开 XML**，选择需要处理的旧路径以及新目标目录。
4. **运行 Scan / Dry Run 预演。** 检查曲目所在位置、Playlist 归属、无 Playlist 曲目、缺失文件、磁盘空间和冲突。
5. **执行复制和校验。** 保留相对目录结构，输出迁移结果与**旧路径 → 新路径映射**；可选择严格 SHA-256 文件校验。
6. **回到 Rekordbox**，使用官方 **Relocate / Auto Relocate** 将原有曲目重新关联至新位置，然后检查 Playlist、Cue 点、Beatgrid 等数据。

**重要：RB Rescue 不会自动修改 Rekordbox 中的文件路径。** 最后一步需要你在 Rekordbox 内完成；能否保留原有曲库关联，取决于是否正确执行并确认 Relocate 操作。

### RB Rescue 能做什么？

- 根据 **Rekordbox XML** 分析曲目原有路径，不读取或修改 Rekordbox 私有数据库。
- 让用户自主选择需要迁移的来源路径，而不是盲目复制整个 U 盘。
- 区分**属于至少一个 Playlist** 和**完全不属于任何 Playlist** 的音乐，分别放入 `Recovered_With_Playlist` 与 `Recovered_No_Playlist`，同时保留源文件的相对目录结构。**不会按每一个 Playlist 分别创建文件夹。**
- 通过 **Dry Run** 提前发现缺失文件、目标路径冲突等问题。
- **仅复制、不删除源文件、不主动覆盖已有文件**；支持中断恢复、文件校验和结果报告。
- 提供**简体中文 / 英语**双语界面。

### 下载与系统要求

1. 到 [Releases 页面](https://github.com/Marhumeltu/rb-rescue-releases/releases/latest)下载 `RBRescue-v0.1.0-win64.zip`。
2. 解压到本地目录，启动其中的程序。
3. 准备 Rekordbox XML 和可以正常读取的旧存储设备，按上述流程操作。

- **平台：** 目标为 Windows 10/11 x64；已在 **Windows 11 Sandbox** 环境验证，Windows 10 **尚未独立验证**。
- **运行依赖：** [Microsoft Visual C++ Redistributable (x64)](https://aka.ms/vc14/vc_redist.x64.exe)。

### 安全说明与功能边界

**开始前请备份 Rekordbox 曲库和原始音乐文件。** 源音乐必须仍然可读取。RB Rescue 不是数据恢复软件，不能修复已经损坏的音频、恢复无法访问的旧盘、自动查找已经丢失的文件，也不会直接修复 Rekordbox 内部的 Missing Files 路径。请认真检查 Dry Run 与目标目录，并在完成 Relocate 后确认曲库信息无误。

### 第三方许可证与源码

应用包包含适用的第三方许可证、版权与 attribution 材料，以及 LGPL 库替换说明。同一 [Release 页面](https://github.com/Marhumeltu/rb-rescue-releases/releases/latest)提供独立的第三方源码附件。

随附文档如实记录了部分上游源码和版权归属材料与预编译第三方二进制之间尚未完全确认的对应关系。本仓库不公开 RB Rescue 自身开发源码，但不影响第三方组件适用的许可证和用户权利。

**免责声明：** RB Rescue 是独立开发项目，与 AlphaTheta 或 Pioneer DJ 不存在官方关联、赞助或认可关系。

---

**Move the files. Reconnect the tracks. Keep the work you've put into your library.**  
**迁移音频文件，重新关联原有曲目，保留你多年整理曲库的心血。**
