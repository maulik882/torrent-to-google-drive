# 📖 Complete Usage Guide

## Table of Contents
- [Getting Started](#getting-started)
- [Step-by-Step Tutorial](#step-by-step-tutorial)
- [FAQ](#faq)
- [Tips & Tricks](#tips--tricks)
- [Troubleshooting](#troubleshooting)

---

## Getting Started

### What You Need
1. A Google account (free)
2. Internet connection
3. A torrent file or magnet link

### What You DON'T Need
- ❌ No software installation
- ❌ No credit card
- ❌ No technical skills
- ❌ No local storage

---

## Step-by-Step Tutorial

### 1️⃣ Open the Notebook

**Option A: Via GitHub**
1. Go to the repository
2. Click on `Torrent_to_Google_Drive.ipynb`
3. Click "Open in Colab" badge at the top

**Option B: Direct Link**
Click: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maulik882/torrent-to-google-drive/blob/main/Torrent_to_Google_Drive.ipynb)

### 2️⃣ Run Cell 1 (Install Dependencies)

**What it does**: Installs libtorrent library (~30 seconds)

**Steps**:
1. Click the ▶️ play button on the left of Cell 1
2. Wait for the green checkmark ✅
3. You should see "✅ All dependencies ready!"

**If you see an error**:
- Go to `Runtime` → `Change runtime type`
- Select `Python 3.10`
- Click `Save`
- Run Cell 1 again

### 3️⃣ Run Cell 2 (Initialize Engine)

**What it does**: Sets up the torrent download engine

**Steps**:
1. Click the ▶️ play button on Cell 2
2. Wait ~2 seconds
3. You should see "✅ libtorrent session initialized!"

### 4️⃣ Run Cell 3 (Connect Google Drive)

**What it does**: Gives permission to save files to your Drive

**Steps**:
1. Click the ▶️ play button on Cell 3
2. A popup will ask "Permit this notebook to access your Google Drive?"
3. Click **"Connect to Google Drive"**
4. Choose your Google account
5. Click **"Allow"**
6. You should see "✅ Google Drive mounted!"

**Important**: Your files will be saved in `My Drive/Torrents/`

### 5️⃣ Add Your Torrent

**OPTION A: Upload .torrent File (Cell 4)**

1. Run Cell 4
2. Click **"Choose Files"** button that appears
3. Select your .torrent file(s) from your computer
4. Click **"Open"**
5. Wait for upload to complete
6. You'll see: "✅ Added: [filename]"

**You can upload multiple files at once!**

**OPTION B: Use Magnet Link (Cell 5)**

1. Copy your magnet link (starts with `magnet:?xt=urn:btih:...`)
2. Run Cell 5
3. Paste the magnet link when prompted
4. Press Enter
5. You'll see: "✅ Magnet link added!"

### 6️⃣ Run Cell 6 (Monitor Downloads)

**What it does**: Shows live download progress

**What you'll see**:
- Progress bars for each download
- Download speed (⬇️)
- Upload speed (⬆️)
- Number of connected peers (👥)
- Current state (downloading/seeding)
- Percentage complete

**Example**:
```
📦 ubuntu-22.04.iso
⬇️ 2450.5 KB/s | ⬆️ 120.3 KB/s | 👥 15 peers | downloading | 45.3%
[████████████░░░░░░░░░░] 45.3%
```

**How long will it take?**
- Depends on torrent size and number of seeders
- Well-seeded torrents: Usually fast (5-20 MB/s)
- Poorly seeded: Can be slow (<1 MB/s)

**Can I leave the tab?**
- ❌ No! Keep the browser tab open
- If you close it, the download will stop

### 7️⃣ Run Cell 7 (Get File Links)

**What it does**: Creates clickable links to your downloaded files

**What you'll see**:
```
📁 Files in Google Drive/Torrents:

📄 ubuntu-22.04.iso
   Size: 3450.23 MB
   🔗 Link: https://drive.google.com/file/d/xxxxx/view

📊 Total: 1 files, 3.37 GB
```

**Below that**: Beautiful clickable buttons to open each file

**Click the links to**:
- View the file in Google Drive
- Download to your computer
- Share with others
- Move to another folder

---

## FAQ

### Q: Is this legal?
**A**: Yes, the tool itself is legal. However, you must only download content you have rights to access (Linux ISOs, open-source software, public domain content, etc.)

### Q: Is it really free?
**A**: Yes! Google Colab is free. No hidden costs, no subscriptions.

### Q: How much can I download?
**A**: Limited by:
- Your Google Drive storage (15GB free)
- Colab session time (~12 hours)
- No bandwidth limits

### Q: Can I download multiple torrents at once?
**A**: Yes! Upload multiple .torrent files in Cell 4, then run Cell 6 once. They'll all download in parallel.

### Q: What happens after 12 hours?
**A**: The session expires. Any completed downloads remain in your Drive. Incomplete downloads are lost.

### Q: Can I close my computer while downloading?
**A**: No. Keep the browser tab open on an active device.

### Q: What file types are supported?
**A**: All types! Videos, ISOs, archives, documents - anything in a torrent.

### Q: Can others see my downloads?
**A**: No. Files go to YOUR Google Drive. Private and secure.

### Q: Is my Google account safe?
**A**: Yes. The notebook only requests Drive access (to save files). No other permissions.

---

## Tips & Tricks

### 🎯 Maximize Download Speed
1. Choose torrents with many seeders (100+)
2. Download during off-peak hours (late night/early morning)
3. Use multiple smaller torrents instead of one huge file

### 🎯 Download Large Files
1. Make sure you have enough Drive storage
2. Start downloads early (don't wait until hour 11)
3. Check progress regularly

### 🎯 Organize Your Downloads
After Cell 7, in Google Drive:
1. Open the `Torrents` folder
2. Create subfolders (Movies, Software, etc.)
3. Move files to organize them

### 🎯 Share Your Downloads
1. Run Cell 7 to get links
2. Open file in Drive
3. Click "Share" button
4. Set permissions and share the link

### 🎯 Save Time on Repeat Downloads
1. Keep the Colab tab open
2. After first download completes, go back to Cell 4 or 5
3. Add another torrent
4. Run Cell 6 again

---

## Troubleshooting

### Problem: Cell 1 fails with "Python 3.12 error"
**Solution**: 
1. `Runtime` → `Change runtime type` → `Python 3.10` → `Save`
2. Run Cell 1 again

### Problem: "Permission denied" when running Cell 3
**Solution**: 
1. Make sure you clicked "Allow" on the permission popup
2. If popup didn't appear, run Cell 3 again

### Problem: Download is stuck at 0%
**Possible causes**:
- Magnet link needs time to fetch metadata (wait 2-3 minutes)
- No seeders available (try a different torrent)
- Connection issue (check your internet)

### Problem: "Out of storage" error
**Solution**: 
1. Free up space in your Google Drive
2. Delete old files
3. Or upgrade to Google One for more storage

### Problem: Downloads are very slow
**Causes**:
- Few seeders (check torrent health before downloading)
- Peak usage time (try during off-hours)
- Large file size (be patient)

### Problem: Session disconnected
**Solution**: 
- Your session timed out or connection lost
- Completed downloads are still in your Drive
- Restart from Cell 1 for new downloads

### Problem: Can't find my files
**Solution**: 
1. Run Cell 7 for direct links
2. Or manually check: `My Drive` → `Torrents` folder in Google Drive

### Problem: Download stopped halfway
**Causes**:
- Browser tab was closed
- Internet connection lost
- Session timed out (12 hour limit)

**Solution**: Restart and try again (previous partial downloads are lost)

---

## Best Practices

### ✅ DO:
- Use for legal content only
- Keep browser tab open during downloads
- Check your Drive storage before large downloads
- Run Cell 7 after downloads complete
- Star the GitHub repo if you find it useful!

### ❌ DON'T:
- Download copyrighted content without permission
- Close the browser tab during downloads
- Use for illegal activity
- Share your Google account credentials
- Expect instant downloads (torrents take time)

---

## Need More Help?

- 🐛 [Report a Bug](https://github.com/maulik882/torrent-to-google-drive/issues)
- 💬 [Ask a Question](https://github.com/maulik882/torrent-to-google-drive/discussions)
- 📧 Contact: [Open an Issue](https://github.com/maulik882/torrent-to-google-drive/issues)

---

**Happy Downloading! 🚀**

Remember: Use responsibly and legally!
