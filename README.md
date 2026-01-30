# 🎞️ vls (Visual Video Lister)

vls is a high-performance, visual CLI alternative to ls for media files. It
generates beautiful, informative preview cards directly in your terminal,
featuring technical metadata and high-quality thumbnails, all wrapped in the
Dracula color scheme.

## 🚀 Features

Smart Inode Caching: Uses a persistent hashing system based on File Inode and
Modification Time. Pre-rendered cards are stored in ~/.cache/vls, making
subsequent listings near-instant.

**Rich Metadata**: Automatically extracts and displays:

**Video Codec** (e.g., H264, HEVC, VP9).

**Precise Duration** (Sexagesimal format HH:MM:SS).

**File Size** (Human-readable).

**Robust UI**: Fixed-canvas rendering using ImageMagick ensures consistent font
sizes and perfect vertical alignment regardless of filename length.

**Dracula Aesthetics**: Styled with the Dracula color palette for a premium terminal
experience.

## 🛠 Dependencies

You will need the following tools installed:

**ffmpeg** (for ffprobe metadata extraction)

**ImageMagick 7** (for image composition)

**ffmpegthumbnailer** (for fast thumbnail generation)

**viu** (for terminal image rendering)

**0xProto Nerd Font** (for icons and typography)

## 📦 Installation

To install vls system-wide, follow these steps:

Make the script executable:

```bash

chmod +x vls.sh
```

Move it to the system binary directory:

```bash

sudo mv vls.sh /usr/local/bin/vls
```

Verify the installation: You can now run vls from any directory.

## 🖥 Usage

Simply navigate to a folder containing videos and run:

```bash

vls
```

⚙️ Configuration

The script stores its cache in ~/.cache/vls. If you want to force a refresh of
the thumbnails (for example, after changing the font or colors), simply clear
the cache:

```bash

rm -rf ~/.cache/vls/\*
```

## ⚖️ License

Copyright (C) 2026 Hugo Morago Martín

This project is licensed under the **GNU General Public License v3.0**. See the
[LICENSE](LICENSE) file for the full text and details.
