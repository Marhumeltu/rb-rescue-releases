# RB Rescue

**A safer way to migrate your Rekordbox music library.**

**更安全地迁移你的 Rekordbox 音乐曲库。**

RB Rescue is a free, portable Windows utility designed for DJs who need to migrate and reorganize music files using a Rekordbox XML library export.

RB Rescue 是一款免费的 Windows 便携式工具，帮助 DJ 通过 Rekordbox 导出的 XML 曲库文件，安全地迁移与重新整理音乐文件。

[**Download / 下载最新版本**](https://github.com/Marhumeltu/rb-rescue-releases/releases)

---

## English

### Features

- **XML-based migration** — Reads Rekordbox XML exports without modifying the internal Rekordbox database.
- **Playlist-aware organization** — Separates tracks referenced by playlists from tracks without playlist membership.
- **Dry Run preview** — Review the migration plan before copying any files.
- **Conflict protection** — Detects missing files, destination conflicts and potential overwrites.
- **Copy-only workflow** — Leaves original music files untouched.
- **Integrity verification** — Optional strict SHA-256 verification.
- **Resumable operations** — Supports continuing interrupted migration jobs.
- **Bilingual interface** — English and Simplified Chinese.

### Download & Installation

1. Visit [Releases](https://github.com/Marhumeltu/rb-rescue-releases/releases).
2. Download `RBRescue-v0.1.0-win64.zip`.
3. Extract the ZIP to a local folder.
4. Launch the included RB Rescue application.
5. Export your Rekordbox collection as XML and select it in RB Rescue.

**System requirements**

- Windows 10/11 x64 target
- Validated in a Windows 11 Sandbox environment; Windows 10 has not been independently validated
- [Microsoft Visual C++ Redistributable (x64)](https://aka.ms/vc14/vc_redist.x64.exe) required

### Important Safety Information

RB Rescue does not modify the original Rekordbox database or delete source music files.

Always review the Dry Run results, verify your destination folder and maintain an independent backup before migration.

### Licenses & Third-Party Sources

Applicable third-party licenses, copyright notices and LGPL library replacement instructions are provided with the application.

Third-party source materials are distributed separately as `RBRescue-v0.1.0-third-party-sources.zip` in the same GitHub Release.

The included documentation describes component provenance and known limitations in upstream-to-binary traceability.

RB Rescue's own development source code is not distributed in this repository. This does not affect the license terms and rights applicable to included third-party components.

### Disclaimer

RB Rescue is an independent project and is not affiliated with, sponsored by or endorsed by AlphaTheta or Pioneer DJ.

---

## 简体中文

### 主要功能

- **基于 XML 的曲库迁移** — 读取 Rekordbox 导出的 XML 曲库，不修改 Rekordbox 内部数据库。
- **播放列表识别** — 根据曲目是否属于播放列表，将音乐文件分别整理。
- **Dry Run 预演** — 正式复制前预览迁移计划及执行结果。
- **文件冲突保护** — 识别缺失文件、目标路径冲突和潜在覆盖风险。
- **仅复制模式** — 保留源音乐文件，不执行删除操作。
- **完整性校验** — 支持可选的严格 SHA-256 文件校验。
- **中断续传** — 支持恢复意外中断的迁移任务。
- **双语界面** — 支持英语与简体中文。

### 下载与安装

1. 打开 [Releases 发布页面](https://github.com/Marhumeltu/rb-rescue-releases/releases)。
2. 下载 `RBRescue-v0.1.0-win64.zip`。
3. 将 ZIP 解压至本地文件夹。
4. 启动其中的 RB Rescue 程序。
5. 从 Rekordbox 导出 XML 曲库文件，并在 RB Rescue 中选择该文件。

**系统要求**

- 目标平台：Windows 10/11 x64
- 已通过 Windows 11 Sandbox 环境验证；Windows 10 尚未独立验证
- 需要安装 [Microsoft Visual C++ Redistributable (x64)](https://aka.ms/vc14/vc_redist.x64.exe)

### 重要安全说明

RB Rescue 不会修改原始 Rekordbox 数据库，也不会删除源音乐文件。

执行迁移前，请务必检查 Dry Run 预演结果、确认目标文件夹，并保留独立的曲库备份。

### 开源许可证与第三方源码

程序随附适用的第三方许可证、版权声明及 LGPL 库替换说明。

第三方源码材料通过同一 GitHub Release 中的 `RBRescue-v0.1.0-third-party-sources.zip` 独立提供。

随附文档记录了第三方组件来源，以及部分上游源码与预编译二进制之间尚未完全确认的对应关系。

本仓库不公开 RB Rescue 自身的开发源代码，但不影响所包含第三方组件适用的许可证条款及用户权利。

### 免责声明

RB Rescue 是独立开发项目，与 AlphaTheta 或 Pioneer DJ 不存在官方关联、赞助或认可关系。

---

**Made for DJs who care about their music libraries.**

**为认真对待自己音乐曲库的 DJ 而打造。**
