# RB Rescue

**Move your music. Keep your Rekordbox library.**  
**迁移音乐，而不是重建你的 Rekordbox 曲库。**

**Is your Rekordbox collection still tied to an old DJ USB drive, external SSD, or hard drive?** You want to move the audio files to your computer or a new disk, but you don't want to re-import thousands of tracks and lose the connection to playlists, cues, beatgrids, and other work you've already done.

**你的 Rekordbox 曲库还依赖旧 U 盘、移动 SSD 或硬盘吗？** 想把音乐迁移到电脑或新硬盘，却不想重新导入上万首曲目，更不想让多年整理的 Playlist、Cue 点和 Beatgrid 等资料失去关联？

**RB Rescue is built for exactly this situation. / RB Rescue 就是为解决这个问题而开发的。**

[**Download v0.1.0 / 下载 v0.1.0**](https://github.com/Marhumeltu/rb-rescue-releases/releases/latest) · [English](#english) · [简体中文](#简体中文)

---

## English

### The problem

When you export music to a DJ USB drive, Rekordbox may still store track locations pointing to that drive (for example, `J:\Contents\Artist\Album\Track.mp3`). Replacing the drive or moving your music files doesn't automatically update those paths inside your existing collection.

Re-importing the same files as new tracks isn't a good substitute if you've spent years maintaining playlists, hot cues, beatgrids, ratings, and comments. And manually sorting thousands of files—especially tracks scattered through a `Contents/Artist/Album` directory—is time-consuming and error-prone.

**RB Rescue helps you move the underlying audio files while keeping the existing Rekordbox collection as the collection you intend to reconnect.** It reads a Rekordbox XML export, identifies track locations and playlist membership, copies selected files safely, and produces old-to-new path mappings. **You then complete the reconnection using Rekordbox's own Relocate / Auto Relocate tools.**

### How it works

1. **Export XML from Rekordbox.** Keep your existing Rekordbox library and make a backup before starting.
2. **Select the XML and source location(s).** RB Rescue discovers file locations; you choose which old drive or folder to migrate.
3. **Choose a destination and run Scan / Dry Run.** Review file counts, playlist membership, missing files, disk space, and conflicts before copying.
4. **Copy and verify.** RB Rescue copies the selected audio files without deleting the originals, preserves relative directory structure, and generates migration results and path mappings. Optional strict SHA-256 verification is available.
5. **Relocate inside Rekordbox.** Use Rekordbox's official Relocate / Auto Relocate workflow to reconnect your *existing* tracks to the new locations. Then check playlists, cues, beatgrids, and other library data.

> **Important:** RB Rescue does **not** automatically update track locations in Rekordbox or directly edit its private database. Successful preservation of existing library associations depends on completing and checking the Relocate step.

### What makes it useful?

- **Existing collection first:** Work from a Rekordbox XML export instead of rebuilding the collection through bulk re-import.
- **Playlist-aware migration:** Separate tracks that belong to at least one playlist from tracks with no playlist membership. This is **not** an export of each individual playlist into a folder.
- **Predictable folders:** Preserve the selected source's relative folder structure under `Recovered_With_Playlist` and `Recovered_No_Playlist`.
- **Preview before copying:** Detect missing files, insufficient space, and destination conflicts rather than blindly moving a large collection.
- **Safer copying:** Copy-only workflow, overwrite protection, optional SHA-256 verification, resumable operations, and result reports.
- **Bilingual interface:** English and Simplified Chinese.

### Download & installation

1. Download [`RBRescue-v0.1.0-win64.zip`](https://github.com/Marhumeltu/rb-rescue-releases/releases/latest).
2. Extract the ZIP to a local folder and launch the included RB Rescue application.
3. Export your Rekordbox collection to XML, then follow the workflow above.

**System requirements**

- Windows 10/11 x64 target; **validated in Windows 11 Sandbox**. Windows 10 has not been independently validated.
- [Microsoft Visual C++ Redistributable (x64)](https://aka.ms/vc14/vc_redist.x64.exe) must be installed.

### Safety and limitations

- **Back up your Rekordbox library and audio files before migrating.**
- Source audio files must still be readable. RB Rescue is **not** a repair tool for a failed drive or corrupted audio.
- RB Rescue does not delete source audio, directly modify Rekordbox's private database, or automatically perform Relocate.
- Review Dry Run results and the destination carefully; verify the Rekordbox library after reconnecting your tracks.

### Third-party licenses & source materials

The application distribution includes applicable third-party license texts, copyright/attribution materials, and LGPL library replacement instructions. A separate [third-party source archive](https://github.com/Marhumeltu/rb-rescue-releases/releases/latest) is provided alongside the Windows download.

The included documents also describe known limits in matching some upstream source and attribution materials to precompiled third-party binaries. This repository does **not** publish RB Rescue's own development source code; rights under third-party licenses remain unaffected.

**Disclaimer:** RB Rescue is an independent project, not affiliated with, sponsored by, or endorsed by AlphaTheta or Pioneer DJ.

---

## 简体中文

### 为什么需要 RB Rescue？

Rekordbox Collection 中记录的音乐文件路径，可能仍然指向你多年前使用的 DJ U 盘或外置硬盘，例如 `J:\Contents\Artist\Album\Track.mp3`。即便你将这些文件复制到电脑或新硬盘，**Rekordbox 并不会因此自动更新原有曲目的文件位置**。

如果你花了多年整理 Playlist、Hot Cue、Beatgrid、Rating 和 Comment，直接把音乐重新 Import 成新曲目并不是理想的解决办法：你可能失去新文件与原有曲库记录之间的关联。此外，DJ U 盘的 `Contents/Artist/Album` 自动目录结构，也让手工筛选和整理成千上万首音乐变得困难。

**RB Rescue 的目标，是帮助你搬迁实际音频文件，而不是让你从零重建曲库。** 它读取 Rekordbox 导出的 XML，识别各首曲目的原始路径及 Playlist 归属，安全复制选定文件，并生成旧路径到新路径的映射。**最后，由你使用 Rekordbox 官方 Relocate / Auto Relocate 功能重新关联原有曲目。**

### 使用流程

1. **从 Rekordbox 导出 XML。** 保留现有 Rekordbox 曲库，并提前做好备份。
2. **选择 XML 与源路径。** RB Rescue 分析曲目实际位置；由你指定需要迁移的旧 U 盘、硬盘或文件夹。
3. **选择目标目录并运行 Scan / Dry Run。** 在复制前检查文件数量、Playlist 归属、缺失文件、剩余空间和冲突情况。
4. **安全复制并校验。** 保留原音乐文件和相对目录结构，生成迁移结果与路径映射，并支持可选的严格 SHA-256 校验。
5. **回到 Rekordbox 完成 Relocate。** 使用官方 Relocate / Auto Relocate，让原有曲目重新指向新位置，再核对 Playlist、Cue 点、Beatgrid 等信息。

> **重要：** RB Rescue **不会自动修改 Rekordbox 中的曲目路径，也不会直接修改其私有数据库**。要保留原有曲库关联，必须正确完成并检查后续 Relocate 操作。

### 核心功能

- **围绕现有 Collection 迁移：** 以 Rekordbox XML 为分析依据，无需通过大批量重新 Import 来重建曲库。
- **识别 Playlist 归属：** 区分至少属于一个 Playlist 的曲目与完全没有 Playlist 归属的曲目；**不是**将每个 Playlist 单独导出为文件夹。
- **保留物理目录结构：** 在 `Recovered_With_Playlist` 与 `Recovered_No_Playlist` 下保留原始相对路径。
- **先预演再复制：** 提前识别缺失文件、空间不足与目标路径冲突。
- **安全优先：** 仅复制、不覆盖既有文件、支持可选 SHA-256 校验、中断恢复和结果报告。
- **中英文界面：** 支持简体中文和英语。

### 下载与安装

1. 在 [Releases 页面](https://github.com/Marhumeltu/rb-rescue-releases/releases/latest)下载 `RBRescue-v0.1.0-win64.zip`。
2. 解压到本地文件夹，运行其中的 RB Rescue 程序。
3. 从 Rekordbox 导出 XML，然后按上述步骤操作。

**系统要求**

- 目标平台：Windows 10/11 x64；**已在 Windows 11 Sandbox 中验证**，Windows 10 尚未独立验证。
- 需要安装 [Microsoft Visual C++ Redistributable (x64)](https://aka.ms/vc14/vc_redist.x64.exe)。

### 安全说明与适用范围

- **迁移前请备份 Rekordbox 曲库和原始音频文件。**
- 源音乐文件必须仍然可以正常读取；RB Rescue **不是**损坏硬盘或损坏音频的数据恢复工具。
- 不删除源文件、不直接修改 Rekordbox 私有数据库，也不会自动执行 Relocate。
- 正式复制前核对 Dry Run 与目标目录；完成重新关联后检查 Rekordbox 曲库数据。

### 第三方许可证与源码

应用发行包内含适用的第三方许可证、版权及 attribution 材料，以及 LGPL 库替换说明。同一 [Release 页面](https://github.com/Marhumeltu/rb-rescue-releases/releases/latest)另附第三方源码 ZIP。

随附文档也如实记录了部分上游源码、版权归属材料与预编译第三方二进制之间尚未完全确认的对应关系。本仓库不公开 RB Rescue 自身的开发源码，但不影响第三方组件的许可证及接收者权利。

**免责声明：** RB Rescue 是独立开发项目，与 AlphaTheta 或 Pioneer DJ 不存在官方关联、赞助或认可关系。

---

**Made for DJs who care about their music libraries.**  
**为认真对待自己音乐曲库的 DJ 而打造。**
