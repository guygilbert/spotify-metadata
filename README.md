# 🎵 Spotify Playlist Exporter

A lightweight Python utility to export a public Spotify playlist — including audio features like **energy, danceability, valence, tempo, key**, and more — into a clean CSV file.

---

## 🧰 Features
- Works on **public playlists** (no login needed)
- Uses Spotify’s Web API with your own developer credentials
- Automatically fetches:
  - Track name, artist, album, release date
  - Popularity and explicit flag
  - Audio features (energy, valence, tempo, loudness, etc.)
- Exports results to `playlist_tracks_with_features.csv`
- Safe `.gitignore` to protect your secrets and data

---

## ⚙️ Setup

### 1. Requirements
- Python 3.9 or newer  
- A Spotify developer account ([create one here](https://developer.spotify.com/dashboard))  
- Internet connection

### 2. Get your API credentials
1. Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Click **Create an App**
3. Copy your **Client ID** and **Client Secret**
4. In the project folder, create a file named `.env` and add:
SPOTIFY_CLIENT_ID=your_client_id_here
SPOTIFY_CLIENT_SECRET=your_client_secret_here


---

## ▶️ Run the Export

### Option A: One-click (Windows)
Double-click **`run_export.bat`**

### Option B: Command line
python spotify_export.py --playlist "https://open.spotify.com/playlist/0NxadBPJqpM4yKfoRfRseI" --out "playlist_tracks_with_features.csv"

📁 Output

The script saves a CSV file containing columns like:
Column	Description
track_name	Song title
artist	Artist(s)
danceability	0–1 float
energy	0–1 float
valence	0–1 mood positivity
tempo	BPM
key_name	Musical key
popularity	Spotify popularity (0–100)
...	and more

💡 Tips
Works best on an unrestricted network (some VPNs block the Spotify API)
If the window closes too fast, run it from Command Prompt to read errors
Keep your .env file private — it’s ignored by GitHub automatically

📜 License
MIT License © [Your Name or Alias]

✨ Example
Playlist: Happy B'Day David — by Guy Gilbert (21 tracks)
Saved 21 rows to playlist_tracks_with_features.csv

🧩 Project structure
spotify-playlist-exporter/
 ├─ .gitignore
 ├─ README.md
 ├─ .env                # your Spotify credentials (local only)
 ├─ spotify_export.py
 ├─ run_export.bat
 └─ playlist_tracks_with_features.csv

 🚀 Future ideas
- Add automatic genre or mood classification
- Support for private playlists (OAuth)
- Simple web UI for upload/export
  
Happy exporting! 🎧
