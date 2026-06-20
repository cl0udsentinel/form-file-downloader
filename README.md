# 📋 FormFiles — Google Form Response File Downloader

A simple, browser-based tool to download files from **Google Form response sheets**. Select any row and download all its file attachments as a ZIP — no coding or installation required.

---

## ✨ Features

- 📂 **Load multiple Google Sheet files** at once with tabs to switch between them
- 🔍 **Auto-detects file URL columns** from your Form response sheet
- 🖱️ **Click any row** to preview and download its files
- 🗜️ **Download all files as a ZIP** in one click
- 📁 **Google Drive links** open in a new tab (Ctrl+S to save)
- 💾 **Save your config** (API key + Sheet IDs) to a JSON file so you don't re-enter every time
- 🔎 **Search/filter rows** by any value
- ✅ Works entirely in the browser — no backend, no installation

---

## 🚀 How to Use

### 1. Get a Google Sheets API Key (Free)

1. Go to [console.cloud.google.com](https://console.cloud.google.com)
2. Create a project → enable **Google Sheets API**
3. Go to **Credentials** → **Create Credentials** → **API Key**
4. Copy your API key (starts with `AIza…`)

### 2. Share your Google Sheet

- Open your Google Form response sheet
- Click **Share** → **Anyone with the link** → **Viewer** → Done

### 3. Get your Spreadsheet ID

From the sheet URL:
```
https://docs.google.com/spreadsheets/d/SPREADSHEET_ID_HERE/edit
```
Copy the long string between `/d/` and `/edit`

### 4. Open the App

Open the app at:
```
https://YourUsername.github.io/form-file-downloader/form_file_downloader.html
```

### 5. Enter Details & Load

- Paste your **API Key** and **Spreadsheet ID(s)**
- Click **💾 Save Config** to save them for next time
- Click **⚡ Load Sheets**
- Select a row → click **🗜️ Download ZIP**

---

## 💾 Saving Your Config

Click **💾 Save Config** to download a `formfiles-config.json` file.  
Next time, click **📂 Load Config** to restore your API key and all Sheet IDs instantly.

> ⚠️ Keep your config file safe — it contains your API key.

---

## 📁 File Types Handled

| Type | How it's downloaded |
|------|-------------------|
| Direct files (`.pdf`, `.jpg`, `.zip`, etc.) | Auto-downloaded and zipped |
| Google Drive links | Opens in new tab → press Ctrl+S to save |

---

## 🛠️ Troubleshooting

| Error | Fix |
|-------|-----|
| `Failed to load` | Check API key starts with `AIza`, Sheet ID is correct, Sheets API is enabled |
| `Network error` | Must be opened via `https://` — not from `file://` on your computer |
| `CORS blocked` | Google Drive files can't be fetched directly — use the ↗ open button |
| `Access denied (403)` | Make sure the sheet is shared as "Anyone with the link can view" |

Use the **🔍 Test Connection** button in the sidebar to diagnose any issue automatically.

---

## 🔧 Tech Stack

- Pure HTML + CSS + JavaScript (no frameworks)
- [Google Sheets API v4](https://developers.google.com/sheets/api)
- [JSZip](https://stuk.github.io/jszip/) for creating ZIP files
- Hosted on GitHub Pages

---

## 📄 License

MIT — free to use, modify, and share.
