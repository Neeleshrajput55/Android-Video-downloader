# 🎬 YouTube Video Downloader Pro (Termux Bash)

> **Developer:** Pummy Rajput  
> **GitHub:** [@Neeleshrajput55](https://github.com/Neeleshrajput55)  
> **Version:** 2.1  
> **Engine:** yt-dlp  
>  
> एक ultimate Termux Bash स्क्रिप्ट, जिससे आप YouTube (या अन्य supported websites) से high-speed और automated तरीके से videos और audios अपने Android मोबाइल की external storage (`/sdcard/YouTube`) में save कर सकते हैं।

***

## ⭐ इस प्रोजेक्ट की खासियत

- **YouTube App से डायरेक्ट Download**: Share से Termux चुनते ही video डाउनलोड।
- **Batch Download**: links.txt में दर्ज कई videos/playlist/channel लिंक को एक साथ डाउनलोड करें।
- **Manual URL Mode**: किसी भी लिंक को सीधे paste करके डाउनलोड करें।
- **Quality Selection**: 144p से 4K (2160p) तक video या केवल audio (MP3) डाउनलोड करें।
- **External Storage Save**: `/sdcard/YouTube` में organized folders (quality/channel/others) में सेविंग।
- **Beautiful Banner & Stats**: Download progress और summary professional look में।
- **No Root Needed**: सिर्फ Termux और permissions।
- **Auto Dependency Install**: yt-dlp, ffmpeg, python खुद install हो जाते हैं।
- **Hinglish + English**: Instructions universal—आप कहीं से भी चला सकते हैं!

***

## 📦 इंस्टॉलेशन (Installation)

### 1. **Termux Install करें**
- F-Droid से [Latest Termux](https://f-droid.org/en/packages/com.termux/) डाउनलोड करें (Play Store से नहीं!)
- Storage Permission दें:  
  ```bash
  termux-setup-storage
  ```

### 2. **स्क्रिप्ट सेव करें और executable बनाएं**

```bash
cp download_videos_termux_v2.1_fixed.sh ~/download_videos.sh
chmod +x ~/download_videos.sh
```

### 3. **अगर YouTube से "Share" Menu से डाउनलोड चाहते हैं:**

- `~/bin/termux-url-opener` bin folder बनाइए और उसमें ये termux-url-opener को bin folder में डालिए:
  ```bash
  #!/data/data/com.termux/files/usr/bin/bash
  mkdir -p ~/bin
  cp termux-url-opener ~/bin/termux-url-opener
  ```
- Executable बनाईये:
  ```bash
  chmod +x ~/bin/termux-url-opener
  ```
- अब YouTube ऐप में कोई video -> Share -> Termux पर tap करें

***

## ⚡ इस्तेमाल कैसे करें (Usage)

### (A) **Direct Share (YouTube App से)**
- वीडियो पर Share → Termux → Quality चुनें → डाउनलोड शुरू

### (B) **Batch Mode (links.txt फाइल से)**
1. `nano links.txt` चलाकर हर line पर एक-एक लिंक लिखें।
2. स्क्रिप्ट चलाएँ:
   ```bash
   ~/download_videos.sh
   ```
3. Download mode में "Download from links.txt" चुनिए।

### (C) **Manual URL Entry**
- स्क्रिप्ट चलाएं, "Enter URL manually" ऑप्शन चुनें, URL paste करें।

***

## 🎞️ Download Location & Folder Structure

```
/sdcard/YouTube/
├── videos/
│   ├── 720p/
│   │   └── ChannelName/
│   ├── 1080p/
│   │   └── ChannelName/
│   └── best_quality/
├── audios/
│   └── ChannelName/
└── playlists/
```

***

## 🎚️ Quality Options (Download Menu में)

- 1 = 144p (Very low, smallest size)
- 2 = 240p  
- 3 = 360p  
- 4 = 480p  
- 5 = 720p (HD, Recommended)  
- 6 = 1080p  
- 7 = 1440p  
- 8 = 2160p (4K)  
- 9 = Best available
- 10 = Audio Only (MP3)

***

## 🏆 Features At A Glance

| Feature                   | Support                    |
|---------------------------|----------------------------|
| Direct YouTube Share      | ✅                        |
| links.txt Batch Download  | ✅                        |
| Manual URL Entry          | ✅                        |
| All Quality Levels        | ✅                        |
| Audio Only (MP3) Mode     | ✅                        |
| Storage: /sdcard/YouTube/ | ✅                        |
| Download Stats Banner     | ✅                        |
| No Root Required          | ✅                        |
| Fast, Reliable & Safe     | ✅                        |

***

## 📱 YouTube Video Downloader Pro - Project Description

**यह script Android पर Termux app का उपयोग करके YouTube और 1000+ अन्य video platforms से videos/audios download करने की क्षमता रखती है।**

### 🎯 मुख्य उद्देश्य:
Android mobile पर बिना किसी third-party app या ads के, सीधे YouTube app से share करके या batch mode में multiple videos को high-quality में download करना।

### 🌐 Supported Platforms:

**YouTube** के अलावा, यह script निम्न platforms से भी download कर सकती है:

- **YouTube** (Videos, Shorts, Playlists, Channels)
- **YouTube Music** (Audio/Music)
- **Facebook** (Videos)
- **Instagram** (Posts, Reels, Stories)
- **Twitter/X** (Videos, GIFs)
- **Vimeo** (Videos)
- **Dailymotion** (Videos)
- **TikTok** (Videos)
- **Reddit** (Videos)
- **Twitch** (Clips, VODs)
- **SoundCloud** (Audio)
- **Bandcamp** (Music)
- और **1000+ websites** (yt-dlp support के अनुसार)

### ⚡ Key Capabilities:

1. **Direct Share Integration** - YouTube app से सीधे Termux में share करके instant download
2. **Batch Processing** - links.txt में multiple URLs से एक साथ download
3. **Quality Selection** - 144p से 4K (2160p) तक या केवल MP3 audio
4. **Smart Organization** - `/sdcard/YouTube` में quality और channel wise folders
5. **No Root Required** - केवल Termux और storage permission चाहिए
6. **Auto-Install Dependencies** - yt-dlp, ffmpeg, python automatic install
7. **Progress Tracking** - Real-time download stats और beautiful UI

### 🎨 Special Features:
- Professional colored banner interface
- Download success/failure statistics
- Metadata और thumbnail embedding
- Concurrent fragment downloading (fast speed)
- Auto-retry on failures
- Empty/comment line handling

**Technology Stack:** Bash scripting, yt-dlp, FFmpeg, Python, Termux environment

***

## ❓ FAQ

- **Q:** Share menu में Termux नहीं दिख रहा?
  **A:** `pkg reinstall termux-tools` करने के बाद bin script executable बनाएं।
- **Q:** Error: links.txt not found?
  **A:** Script खुद बनाएगी – edit करके links डाल सकते हैं।
- **Q:** Download failed?
  **A:** Network, video regional restrictions या server side कारण हो सकता है।
- **Q:** FFmpeg/yt-dlp नहीं है?
  **A:** Script पहली बार अपने आप install करती है।

***

## 🤝 योगदान (Contribution)

सुझाव, pull requests, bug fixes हमेशा स्वागत योग्य हैं! Issue बनाएँ या सीधे PR करें।
- GitHub: [@Neeleshrajput55](https://github.com/Neeleshrajput55)

***

## 👑 क्रेडिट

- Script & UX: **Pummy Rajput**
- yt-dlp & ffmpeg का इस्तेमाल
- आपके सुझावों के लिए धन्यवाद 🙏

***

## 📜 License

**MIT License** — Project को open-source और use/edit करने के लिए आप पूरी तरह आज़ाद हैं!

***

**Enjoy #YouTube Video Downloader Pro — Fast, Reliable, Open-Source, Termux-Ready!**

***
