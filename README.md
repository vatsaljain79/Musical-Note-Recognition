# Musical Note Recognition – Audio Recording Web App

This project is a simple Flask web application that allows users to record audio from their browser, stop the recording whenever they want (max 20 seconds), name the file, and save it locally as an `.mp3`.  
If the filename already exists, the app automatically appends `_1`, `_2`, etc., to avoid overwriting.

---

## Features
- 🎤 Start/stop recording with a single click.
- ⏱ Live timer showing recording length (up to 20 seconds).
- 💾 Automatically saves as `recording1.mp3`, `recording2.mp3`, etc., if no filename is provided.
- 🔄 Appends `_1`, `_2`, etc., if the filename already exists.
- 📥 Option to download the saved audio from the browser.

---

## Requirements
- **Python 3.8+**
- **pip** (Python package manager)
- **ffmpeg** (must be installed and added to PATH)

---

## Installation

### 1️⃣ Clone the repository
```bash
git clone https://github.com/vatsaljain79/Musical-Note-Recognition.git
cd Musical-Note-Recognition
```

### 2️⃣ Install Python dependencies
```bash
pip install flask pydub
```

### 3️⃣ Install FFmpeg
1. Download FFmpeg for Windows:  
   [https://ffmpeg.org/download.html](https://ffmpeg.org/download.html)
2. Extract the zip.
3. Inside the extracted folder, locate the `bin` directory (it contains `ffmpeg.exe`).
4. Add this `bin` path to your **System PATH**:
   - Press `Windows` key → type `Environment Variables` → click **Edit the system environment variables**.
   - Click **Environment Variables**.
   - Under **System variables**, select `Path` → **Edit** → **New** → paste the full `bin` path.
   - Click **OK** on all dialogs.
5. Verify installation:
```bash
ffmpeg -version
```
If it shows version info, you’re good.

---

## Running the App
```bash
python app.py
```
You should see something like:
```
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```

---

## Usage
1. Open your browser and go to [http://127.0.0.1:5000](http://127.0.0.1:5000)
2. Click **Start Recording** 🎤
3. Speak or play sound.
4. Click **Stop Recording** or wait for auto-stop at 20 seconds.
5. Enter a filename (or leave blank for automatic naming).
6. Saved files are stored in the `recordings/` folder.
7. If a filename already exists, it will be saved as `name_1.mp3`, `name_2.mp3`, etc.

---

## Project Structure
```
Musical-Note-Recognition/
│
├── app.py               # Flask backend
├── templates/
│   └── index.html        # Frontend UI
├── recordings/           # Saved audio files
└── README.md
```

---

## Notes
- Works only in browsers that support `MediaRecorder` API.
- If microphone access is blocked, enable it in browser settings.
- On first run, your browser will ask for microphone permission.

---

## License
This project is for educational purposes only. Feel free to modify and use.
