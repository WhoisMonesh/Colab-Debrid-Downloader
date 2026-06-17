# Real-Debrid Torrent Downloader

Offload torrents to Real-Debrid and download directly to Google Drive.

[![Open In Colab](https://colab.research.google.com/assets/github/WhoisMonesh/Colab-Debrid-Downloader/blob/main/Colab-Debrid-Downloader.ipynb)]

---

## Features
| Feature | Description |
|---|---|
| **Sync-safe** | Downloads to local temp, moves to Drive after |
| **Progress Bar** | Real-time HTML progress |
| **Keep-Alive** | Prevents Colab timeout |
| **Auto-Zip** | Zips multiple files with progress + download link |

## How to Use
1. Mount Google Drive
2. Install dependencies
3. Configure variables
4. Run download

### Configuration
| Variable | Default | Description |
|---|---|---|
| `SAVE_PATH` | `/content/downloads/.../` | Local temp dir |
| `DRIVE_PATH` | `/content/drive/My Drive/.../` | Final Drive destination |
| `API_TOKEN` | `""` | Real-Debrid API token |
| `MAGNET_LINK` | `""` | Magnet link to download |
| `KEEP_ALIVE` | `True` | Prevent Colab timeout |

### Requirements
- Real-Debrid account (paid)
- API token from https://real-debrid.com/apitoken

### Why Real-Debrid?
| Torrent2Gdrive | Debrid Downloader |
|---|---|
| Depends on Colab peers | Uses RD cached seedboxes |
| Limited by Colab network | Direct HTTP downloads |
| Slow for rare torrents | Instant if cached |

---

## Technical Details
- Downloads to `/content/downloads/` first, then moves to Drive
- Uses IPython.display HTML for live progress updates
- JavaScript keep-alive prevents session timeout

## Disclaimer
For legal use only.

## License
MIT
