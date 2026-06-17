# Real-Debrid Multi-Source Downloader

Download torrents, direct links, and hoster files via Real-Debrid directly to Google Drive.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/WhoisMonesh/Colab-Debrid-Downloader/blob/main/Colab-Debrid-Downloader.ipynb)

---

## Features
| Feature | Description |
|---|---|
| **Multi-Source** | Torrent magnets + direct links + 1000+ hosters (rapidgator, uploaded, etc.) |
| **Sync-safe** | Downloads to local temp, moves to Drive after |
| **Live Progress** | Real-time HTML progress per file with chunk-level download % |
| **Keep-Alive** | Prevents Colab timeout |
| **Auto-Zip** | Zips multiple files with progress + download link |
| **Large File Safe** | >500 MB files get a Drive link instead of browser download |

## How to Use
1. Mount Google Drive
2. Install dependencies
3. Configure variables (API token + magnet and/or direct URLs)
4. Run download

### Prerequisites
- Real-Debrid account (paid)
- API token from https://real-debrid.com/apitoken

### Configuration
| Variable | Default | Description |
|---|---|---|
| `SAVE_PATH` | `/content/downloads/RealDebridDownloader/` | Local temp dir |
| `DRIVE_PATH` | `/content/drive/My Drive/RealDebridDownloader/` | Final Drive destination |
| `API_TOKEN` | `""` | Real-Debrid API token |
| `MAGNET_LINK` | `""` | Magnet link (torrent) |
| `DIRECT_URLS` | `""` | Comma-separated direct/hoster URLs |
| `KEEP_ALIVE` | `True` | Prevent Colab timeout |

### Supported Sources
- **Torrents** via magnet links (cached = instant, otherwise RD downloads then you grab)
- **File hosters**: RapidGator, Uploaded, NitroFlare, 1Fichier, Turbobit, and [200+ more](https://real-debrid.com/hosters)
- **Direct HTTP/HTTPS links** (premium link generation)

---

## Disclaimer / Fair Use

This tool is provided for **educational and personal use only**. You are responsible for complying with:

| Policy | Notice |
|---|---|
| **Real-Debrid ToS** | Using this tool must comply with Real-Debrid's Terms of Service. |
| **Copyright Law** | Only download content you have the legal right to access. Unauthorized distribution of copyrighted material is prohibited. |
| **Local Laws** | Ensure compliance with applicable copyright laws in your jurisdiction. |

By using this software, you agree to use it **lawfully and responsibly**. The author assumes no liability for misuse.

---

## Technical Details
- Downloads to `/content/downloads/` first, then moves to Drive
- Uses IPython.display HTML for live progress updates at chunk level
- JavaScript keep-alive prevents session timeout
- Large files (>500 MB) skip browser download — use Drive link instead

## License
MIT
