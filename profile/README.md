<p align="center">
  <img
    src="https://avatars.githubusercontent.com/u/328034605?s=400&u=49e2acc19944b34971abaf6678ff6794c3b0fa07&v=4"
    alt="LocMedSec Logo"
    width="180"
  />
</p>

<h1 align="center">LocMedSec</h1>

<p align="center">
  <strong>Local Media Security</strong>
</p>

<p align="center">
  Your Media. Your Device. Your Privacy.
</p>

<p align="center">
  Open-source, privacy-first media tools designed to run locally on your device.
</p>

<p align="center">
  <a href="https://github.com/LocMedSec/locmedsec">Main Project</a> •
  <a href="https://github.com/LocMedSec/locmedsec/issues">Issues</a> •
  <a href="https://github.com/LocMedSec/locmedsec/discussions">Discussions</a> •
  <a href="https://github.com/LocMedSec/locmedsec/blob/main/CONTRIBUTING.md">Contributing</a>
</p>

---

## 🔐 About LocMedSec

**LocMedSec** stands for **Local Media Security**.

We are building an open-source media toolkit focused on one simple principle:

> **Your media should stay under your control.**

LocMedSec aims to make powerful media processing accessible without requiring users to upload their personal files to third-party cloud services.

The project is designed to process media locally on the user's device while providing a simple experience for everyday users and powerful controls for advanced users.

---

## 🎯 Our Mission

We want to make media processing:

* 🔒 **Private** — process files locally whenever possible
* 🌍 **Open** — open source and community driven
* ⚡ **Fast** — use the capabilities of the user's own hardware
* 🛠️ **Powerful** — support professional media workflows
* 🧩 **Extensible** — designed for plugins, presets, and future backends
* 💻 **Cross-platform** — Windows, macOS, and Linux
* ❤️ **Accessible** — simple enough for everyone

---

## ✨ What LocMedSec Aims To Provide

### 🎬 Video

* Format conversion
* Compression
* Resizing
* Cropping
* Trimming
* Merging
* Frame extraction
* Audio extraction
* Codec configuration
* Bitrate and quality control
* Hardware acceleration

### 🎵 Audio

* Audio conversion
* Compression
* Format conversion
* Bitrate control
* Audio extraction
* Metadata handling

### 🖼️ Images

* Format conversion
* Resizing
* Compression
* Transformation
* Metadata handling
* Batch processing

### 📦 Batch Processing

Process multiple files using the same operation or preset.

### 🌐 Media Downloading

Download supported media directly to the user's device where permitted by the source and applicable rights.

### 🔧 Custom Pipelines

Build workflows by combining multiple processing operations.

Example:

```text
Input
  ↓
Resize
  ↓
Remove Metadata
  ↓
Compress
  ↓
Convert
  ↓
Output
```

---

## 🔒 Privacy First

Privacy isn't an additional feature.

**It is part of the architecture.**

LocMedSec is designed around:

* Local-first processing
* No unnecessary cloud uploads
* No mandatory account
* No unnecessary telemetry
* User-controlled files
* Isolated network functionality
* Safe temporary-file handling
* Secure process execution
* Explicit permission boundaries

Media processing should happen on your machine whenever technically possible.

---

## 🏗️ Architecture

LocMedSec is designed as a modular system:

```text
┌───────────────────────────────┐
│       Desktop Application     │
│        Tauri + React          │
└───────────────┬───────────────┘
                │
                ▼
┌───────────────────────────────┐
│          Rust Core             │
│     Application + Domain       │
└───────────────┬───────────────┘
                │
        ┌───────┴────────┐
        ▼                ▼
┌─────────────┐   ┌──────────────┐
│ Job System  │   │   Pipeline   │
│ Queue/Worker│   │   Processing  │
└──────┬──────┘   └───────┬──────┘
       │                   │
       └─────────┬─────────┘
                 ▼
        ┌──────────────────┐
        │     Backends     │
        ├──────────────────┤
        │ FFmpeg           │
        │ libvips          │
        │ yt-dlp           │
        │ Future Backends  │
        └──────────────────┘
```

The core is intentionally independent of the desktop interface so that future applications can reuse the same engine.

---

## 🧰 Technology

LocMedSec is built with open-source technologies including:

| Technology     | Purpose                     |
| -------------- | --------------------------- |
| **Rust**       | Core engine                 |
| **Tauri**      | Desktop application         |
| **React**      | User interface              |
| **TypeScript** | Frontend development        |
| **FFmpeg**     | Video and audio processing  |
| **libvips**    | Image processing            |
| **yt-dlp**     | Supported media downloading |
| **SQLite**     | Local application data      |

---

## 💻 Platforms

LocMedSec is being designed for:

* 🍎 macOS
* 🪟 Windows
* 🐧 Linux

The goal is to provide a consistent experience across platforms while respecting platform-specific capabilities.

---

## 🧩 Designed For Extension

LocMedSec is intentionally modular.

Future community contributions can include:

* New media backends
* New codecs
* New processing operations
* Community presets
* Plugins
* Platform integrations
* Hardware acceleration support
* UI improvements
* CLI tooling
* Automation workflows
* Documentation
* Translations

The architecture is designed so contributors can improve individual parts without needing to understand the entire codebase.

---

## 🗺️ Roadmap

### Phase 1 — Core

* [ ] Rust workspace
* [ ] Media domain model
* [ ] Job abstraction
* [ ] Job queue
* [ ] Worker system
* [ ] FFmpeg backend
* [ ] Media probing
* [ ] Progress reporting
* [ ] Job cancellation
* [ ] Output validation

### Phase 2 — Processing

* [ ] Video conversion
* [ ] Audio conversion
* [ ] Compression
* [ ] Resize
* [ ] Crop
* [ ] Trim
* [ ] Merge
* [ ] Audio extraction
* [ ] Frame extraction
* [ ] Image conversion

### Phase 3 — Desktop

* [ ] Tauri desktop application
* [ ] Drag and drop
* [ ] Job management
* [ ] Progress interface
* [ ] Presets
* [ ] Batch processing
* [ ] Settings
* [ ] Hardware acceleration

### Phase 4 — Downloader

* [ ] Downloader backend
* [ ] Download queue
* [ ] Download progress
* [ ] Format selection
* [ ] Download-to-process pipelines

### Phase 5 — Community

* [ ] Plugin architecture
* [ ] Community presets
* [ ] Localization
* [ ] CLI
* [ ] More platform integrations
* [ ] Contributor ecosystem

---

## 🤝 Community

LocMedSec is built for the community.

There are many ways to contribute:

### 💻 Code

Improve the core, desktop application, processing engines, or platform support.

### 🐛 Bugs

Found something broken?

Open an issue with reproduction steps and relevant system information.

### 💡 Ideas

Have an idea for a useful workflow or feature?

Start a discussion before implementing large changes.

### 🎨 Design

Help improve the user experience, accessibility, icons, layouts, and visual language.

### 🌍 Localization

Help make LocMedSec accessible to users around the world.

### 📚 Documentation

Improve guides, examples, architecture documentation, and onboarding.

---

## 🚀 Contributing

Before contributing, please read:

* [Contributing Guide](https://github.com/LocMedSec/locmedsec/blob/main/CONTRIBUTING.md)
* [Security Policy](https://github.com/LocMedSec/locmedsec/blob/main/SECURITY.md)
* [Code of Conduct](https://github.com/LocMedSec/locmedsec/blob/main/CODE_OF_CONDUCT.md)

We welcome contributions of all sizes.

A documentation fix, bug report, test, translation, or small improvement can be just as valuable as a large feature.

---

## 🔐 Security

Security issues should **not** be reported publicly.

Please follow the project's security policy for responsible disclosure:

[Security Policy](https://github.com/LocMedSec/locmedsec/blob/main/SECURITY.md)

---

## 📜 Open Source

LocMedSec is an open-source project.

We believe powerful media tools should be accessible, transparent, and community driven.

The project welcomes contributors from around the world.

See the repository's `LICENSE` file for the applicable license.

---

## ⭐ Support The Project

If you find LocMedSec useful:

* ⭐ Star the repository
* 🐛 Report bugs
* 💡 Share ideas
* 🔧 Submit improvements
* 📚 Improve documentation
* 🌍 Help with translations
* 📢 Tell others about the project

Every contribution helps.

---

## 🌎 Built For Everyone

LocMedSec is not built around a single operating system, workflow, or type of user.

Whether you're:

* a student,
* developer,
* creator,
* photographer,
* filmmaker,
* researcher,
* privacy-conscious user,
* or simply someone who needs to convert a file,

LocMedSec aims to make the process easier while keeping your data under your control.

---

<p align="center">
  <strong>LocMedSec</strong>
</p>

<p align="center">
  Local Media Security
</p>

<p align="center">
  Your Media. Your Device. Your Privacy.
</p>

<p align="center">
  <sub>Open source • Privacy first • Community driven</sub>
</p>
