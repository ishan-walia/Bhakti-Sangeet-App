![Android](https://img.shields.io/badge/Platform-Android-green)
![Kotlin](https://img.shields.io/badge/Language-Kotlin-blue)
![Firebase](https://img.shields.io/badge/Backend-Firebase-orange)
![Status](https://img.shields.io/badge/Status-Active-success)
![License](https://img.shields.io/badge/License-MIT-purple)
# Bhakti-Sangeet-App

> Simple, easy-to-use devotional music (bhakti) streaming app for Android.

---

## Project Overview

**Bhakti-Sangeet-App** is a mobile app that lets users listen to devotional songs, create playlists, download for offline listening, and follow artists. The app targets Android (Kotlin) but the README keeps guidance general so you can adapt it to other platforms.



## About the App

Bhakti Sangeet is a devotional Android application designed to bring peace and spirituality through beautiful Hanuman Ji Bhajans, Chalisa, Aarti, and more.
The app has a clean UI, fast audio playback, and simple controls for all users.

### Key Features

* Browse devotional songs by category (bhajan, kirtan, aarti, bhajan singer).
* Play / pause / seek audio.
* Create and manage playlists.
* Download songs for offline playback (optional).
* Search songs and artists.
* Favorite (like) songs.
* Background playback with notification controls.
* Simple settings (download quality, theme).

---

## Tech Stack (suggested)

* Android: Kotlin, Jetpack (ViewModel, LiveData), Room (local DB), ExoPlayer (audio), Retrofit (network), Coroutines.
* Backend (optional): Node.js + Express or Firebase (Firestore + Storage).
* Media storage: Cloud Storage (Firebase Storage / S3).

---
## 🔮 Future Scope

- AI Bhajan Recommendation
- Live Aarti Streaming
- Temple Donation Gateway
- Multi-language Voice Control
- Android TV version
## Folder Structure (Android - recommended)

```
app/
 ├── manifests/
 │      └── AndroidManifest.xml
 │
 ├── java/
 │    └── com.example.bhaktisangeet/
 │           ├── activities/
 │           │      ├── Splashscreen.kt           
 │           │      ├── LoginActivity.kt          
 │           │      ├── SignupActivity.kt        
 │           │      ├── MainActivity.kt           
 │           │      ├── MusicActivity.kt         
 │           │      ├── VideoActivity.kt         
 │           │
 │           │      ├── AccountActivity.kt        
 │           │
 │           │      ├── BabaBalakNathJi.kt
 │           │      ├── DurgamataJi.kt
 │           │      ├── GaneshJi.kt
 │           │      ├── HarMahadev.kt
 │           │      ├── HanumanJi.kt
 │           │      ├── KrishnaJi.kt             
 │           │      ├── KhatushyamJi.kt         
 │           │      └── Ramji.kt                
 │           │
 │           ├── adapters/
 │           │      └── (RecyclerView adapters for music, videos)
 │           │
 │           ├── models/
 │           │      ├── SongModel.kt
 │           │      └── VideoModel.kt
 │           │
 │           ├── utils/
 │           │      ├── MediaPlayerHelper.kt      ← (VERY IMPORTANT)
 │           │      ├── ExoPlayerHelper.kt
 │           │      └── SharedPrefs.kt
 │           │
 │           ├── viewmodel/
 │           │      └── (only if you use MVVM)
 │           │
 │           └── data/
 │                 └── Repository.kt
 │
 ├── res/
 │    ├── layout/
 │    │     ├── activity_main.xml
 │    │     ├── activity_music.xml
 │    │     ├── activity_login.xml
 │    │     ├── activity_signup.xml
 │    │     ├── activity_splashscreen.xml
 │    │     ├── activity_account.xml
 │    │     ├── activity_video.xml
 │    │     ├── activity_hanumanji.xml
 │    │     ├── activity_bababalaknathji.xml
 │    │     ├── activity_krishnaji.xml
 │    │     ├── activity_khatushyamji.xml
 │    │     ├── activity_ramji.xml
 │    │     └── row_song_item.xml     (recommended RecyclerView)
 │
res/
 ├── drawable/
 │
 │     ├── gods/
 │     │     ├── ganesh_ji.webp
 │     │     ├── hanuman_ji.png
 │     │     ├── krishna_ji.png
 │     │     ├── ram_ji.png            ← your file (ramji.png)
 │     │     ├── shiva_ji.png          ← your file (shiva.png)
 │     │     ├── durga_mata.png
 │     │     ├── baba_balak_nath.png
 │     │     ├── khatu_shyam_ji.png    ← your file (unnamed.png)
 │     │     └── others…
 │
 │     ├── music_controls/
 │     │     ├── playbutton.png        ← your file (playbutton.png)
 │     │     ├── pause_button.png
 │     │     ├── pause_icon.png
 │     │     ├── btn_next.xml
 │     │     ├── btn_previous.xml
 │     │     ├── btn_repeat.xml
 │     │     └── btn_favorite.xml
 │
 │     ├── icons/
 │     │     ├── ic_home.xml
 │     │     ├── ic_music.xml
 │     │     ├── ic_account.xml
 │     │     ├── ic_search.xml
 │     │     ├── ic_video.xml
 │     │     ├── email.png
 │     │     ├── ema.png
 │     │     ├── lock.png
 │     │     └── pass.png
 │
 │     ├── backgrounds/
 │     │     ├── round_bg_white.xml   
 │     │     ├── search_bg.xml        
 │     │     ├── rounded_white.xml
 │     │     ├── card_rounded.xml
 │     │     ├── border.xml
 │     │     └── saffron_gradient.xml
 │
 │     ├── gradients/
 │     │     ├── bg_gradient.xml
 │     │     └── background_splash_screen.xml
 │
 │     └── misc/
 │           ├── bhakti_app.png
 │           ├── splash_logo.png
 │           └── shape_seekbar_thumb.xml

 │
 │    ├── raw/
 │    │     ├── artiganesh.mp3
 │    │     ├── articri.mp3
 │    │     ├── sya1.mp3
 │    │     ├── ramji1.mp3
 │    │     └── episode1.mp4
 │
 │    ├── menu/
 │    │     └── bottom_nav_menu.xml
 │
 │    └── values/
 │          ├── colors.xml
 │          ├── strings.xml
 │          ├── themes.xml
 │          └── styles.xml
 │
 ├── build.gradle.kts
 └── proguard-rules.pro
```

---

## Quick Start (Android - Kotlin)

### Prerequisites

* Android Studio Flamingo or newer
* JDK 11+
* Internet connection (for streaming)

## 🌐 Supported Devices

- Android Phones
- Android Tablets
- (Android TV – Coming Soon)

## 🎯 Use Cases

✔ College Android Major Project  
✔ Spiritual Audio Streaming App  
✔ Firebase Learning Project  
✔ Ready to Publish on Play Store  
✔ Can be Monetized with Ads  

## ❓ FAQ

Q: Is internet required?
A: Yes, for streaming. Offline works for downloaded songs.

Q: Is this app free?
A: Yes, 100% free.

Q: Can I upload my own bhajans?
A: Admin panel coming soon.


## 🏆 Play Store Ready

- ✔ Privacy Policy
- ✔ AdMob Integration Ready
- ✔ Firebase Auth
- ✔ Offline Mode
- ✔ No Copyright UI Issues
### Install

1. Clone the repo:

```bash
git clone https://github.com/yourusername/Bhakti-Sangeet-App.git
cd Bhakti-Sangeet-App
```

2. Open project in Android Studio and let Gradle sync.

3. Add your API keys and storage configuration in `local.properties` or a secured file (do not commit keys).

## Screenshort
## Screenshots
<p align="center">
  <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page1.png" width="290" style="margin-right:20px;">
  <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page2.png" width="290" style="margin-right:20px;">
  <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page3.png" width="290" style="margin-right:20px;">
  <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page4.png" width="290" style="margin-right:20px;">
  <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page5.png" width="290" style="margin-right:20px;">
    <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page6.png" width="290" style="margin-right:20px;">
  <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page7.png" width="290" style="margin-right:20px;">
  <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page8.png" width="290" style="margin-right:20px;">
    <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page16.png" width="290" style="margin-right:20px;">
  <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page15.png" width="290" style="margin-right:20px;">
  <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page14.png" width="290" style="margin-right:20px;">
  <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page13.png" width="310" style="margin-right:20px;">
   <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page10.png" width="340" style="margin-right:20px;">
  <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page9.png" width="290" style="margin-right:20px;">
 <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page11.png" width="290" style="margin-right:20px;">
 <img src="https://raw.githubusercontent.com/ishan-walia/Bhakti-Sangeet-App/main/Code/Photo/page12.png" width="290" style="margin-right:20px;">
</p>
## API ideas (Backend)

* `GET /songs` — list songs with fields: id, title, artist, url, thumbnail, duration, category
* `GET /songs/{id}` — song details
* `POST /users/{id}/playlists` — create playlist
* `GET /search?q=...` — search songs and artists

---
## 🛠️ Admin Panel (Coming Soon)

- Upload new bhajans
- Delete or update songs
- Send push notifications
- Manage users & playlists
- Festival banners & offers
## Database (Room) — Example entity

```kotlin
@Entity(tableName = "song")
data class Song(
    @PrimaryKey val id: String,
    val title: String,
    val artist: String,
    val url: String,
    val thumbnail: String?,
    val duration: Long
)
```

---

## UI Suggestions

* Home screen with categories and featured songs.
* Now Playing screen with large artwork, play controls, and progress.
* Playlist screen for user playlists and downloads.
* Small persistent player at bottom of lists for quick control.

---

## Offline downloads

* Store downloaded files in app-specific storage.
* Keep a Room table of downloaded tracks and their local paths.
* Check storage space and download quality settings.

---

## Permissions

* `INTERNET` — streaming
* `FOREGROUND_SERVICE` — background playback
* `WRITE_EXTERNAL_STORAGE` / `READ_EXTERNAL_STORAGE` — (only if saving to shared storage; prefer app-specific storage)

---

## Accessibility & Internationalization

* Support large text and talkback labels for buttons.
* Use string resources for easy translation (Hindi, English, Punjabi, etc.).

---

## Testing

* Unit tests for ViewModels and repositories.
* UI tests for playback flows.

---

## Contribution

1. Fork the repository
2. Create a new branch `feature/your-feature`
3. Make changes, add tests
4. Create a Pull Request with description

Please follow a clean commit message style and add screenshots when UI changes are made.

---

## License

This project is MIT licensed — change if you want a different license.

---

## 🏷️ Tags

#Android #Kotlin #Firebase #MusicApp #Bhajan #HanumanJi #MajorProject

## Contact

If you need help: open an issue or contact `your.email@example.com`.

---
## 📲 Download APK

> Direct install on Android:

🔗 **[Download Bhakti Sangeet APK](https://your-apk-link-here.apk)**

Version: 1.0  
Size: ~25 MB  
Minimum Android: 7.0+
### Templates (Optional)

**Issue template**

```
Title: [Bug/Feature] short description
Steps to reproduce:
1.
2.
Expected:
Actual:
```

**Pull request template**

```
Summary of changes:
Related issue:
How tested:
```

### 👨‍💻 Developer

```
Developer Name: Ishan Walia
Campany Name: Walia Creations
Made with Love ❤️ for Devotees of Hanuman Ji
```

*This README is a starter template. Tell me if you want a README specifically for Flutter, React Native, or a full Android Kotlin project — I will create a tailored README.*
🙏 Jai Shri Ram | Jai Hanuman | Har Har Mahadev
