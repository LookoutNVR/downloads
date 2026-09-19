# LookoutNVR downloads

Installers for [LookoutNVR](https://lookoutnvr.com), a self-hosted AI network video recorder.
This repository holds **no source code** — only released installers and the update manifest.

## Download

| | |
|---|---|
| **Recorder (server)** | [LookoutNVR-Server-x64.exe](https://github.com/LookoutNVR/downloads/releases/latest/download/LookoutNVR-Server-x64.exe) |
| **Desktop viewer (client)** | [LookoutNVR-Desktop-x64.exe](https://github.com/LookoutNVR/downloads/releases/latest/download/LookoutNVR-Desktop-x64.exe) |

Those two links always point at the newest release. Every version is also kept, with its version in
the filename, under [Releases](https://github.com/LookoutNVR/downloads/releases).

## Which one do I need?

**The recorder, once.** It watches the cameras and stores the video, runs as a Windows service, and
starts with the machine. Install it on the PC or VM that stays on. Needs an administrator, and the
[.NET 10 runtime](https://dotnet.microsoft.com/download/dotnet/10.0) — setup offers it if missing.

**The viewer, on every PC you watch from.** It connects to the recorder over your network. Installs
per user, so no administrator is needed. Windows 11 already has everything else it requires.

## Or use winget

```powershell
winget install LookoutNVR.Server     # the recorder
winget install LookoutNVR.Desktop    # the viewer
```

Upgrade later with `winget upgrade LookoutNVR.Server`. Note that Windows Server editions do not ship
winget, so use the installer above there.

## Updates

Installed copies check for new versions and tell you; nothing installs itself. The check reads
[update.json](https://github.com/LookoutNVR/downloads/releases/latest/download/update.json) from the
newest release.

---

Issues and support: [lookoutnvr.com/support](https://lookoutnvr.com/support)
