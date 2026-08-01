<!-- Yeh code upar tera bada dark green poster center mein lagayega -->
<p align="center">
  <img src="poster.png" alt="Quest Completer Banner" width="100%">
</p>

# Discord Web Quest Completer Extension

<!-- Yeh code tere icon ko right side mein set karega aur text left mein aayega -->
<img align="right" src="idaa.png" alt="Extension Icon" width="180">

Extension that automatically completes Discord quests. No more manually watching videos or playing massive games - just click a button and let it run quests one by one automatically. Works directly from your browser!
Developed and Designed by **Knowx** ☘️

> [!NOTE]  
> **Disclaimer:** This extension is for educational purposes. Automating user accounts violates Discord's ToS. Use at your own risk.
<br><br>
Original Source from aamiaa 🌸
<br><br>
### ✨ Features
* **🚀 Zero Downloads Needed:** Spoofs the game presence so you don't have to install heavy files.
* **⚡ Lightweight & Fast:** Runs efficiently in your browser without eating up RAM.
* **🖱️ One-Click Automation:** Simple UI to start and track quests.

### 🛠️ How to Install
1. Click on the green **"<> Code"** button at the top right.
2. Select **"Download ZIP"** and extract the file.
3. Open `chrome://extensions/` in your browser.
4. Enable **"Developer mode"**.
5. Click **"Load unpacked"** and select the extracted folder.

What it does
This extension hooks into Discord's quest system and automatically completes the requirements for all active quests sequentially. It works with:

Video watching quests (WATCH_VIDEO, WATCH_VIDEO_ON_MOBILE)
Desktop game playing (PLAY_ON_DESKTOP)
Desktop streaming (STREAM_ON_DESKTOP)
Activity playing (PLAY_ACTIVITY)
The extension spoofs your user-agent to make Discord think you're using the desktop app, which is required for some quest types to work properly. Supports sequential quest execution to ensure stability and proper completion.

Installation
Clone or download this repo
Open Chrome/Edge and go to chrome://extensions/
Toggle "Developer mode" on (top right corner)
Click "Load unpacked" and select the extension folder
You're done!
How to use
Go to https://discord.com/quest-home in your browser
Accept quests if you haven't already
Look for the "Running Quests" button in the bottom right corner with a Symbol icon
Click it and check the browser console (F12) for progress updates
Expand the panel to see quest details (shows Discord ID and credits)
The extension will automatically detect all your active quests and start completing them one by one. Progress is logged to the console so you can see what's happening for each quest.

Requirements
Chrome or any Chromium-based browser (Edge, Brave, etc.)
A Discord account with quests available
Accepted quests on the quest-home page
How it works
The extension uses advanced techniques:

User-Agent override: Modifies HTTP headers and navigator properties to mimic Discord desktop
Webpack module injection: Hooks into Discord's internal stores (QuestsStore, RunningGameStore, etc.)
Multi-quest concurrency: Runs all eligible quests in parallel using Promise.all
API spoofing: Intercepts quest progress updates and sends fake data
Smart detection: Filters quests by expiration and completion status
For streaming quests, you still need at least one other person in the voice channel - the extension can't fake that part.

Troubleshooting
Button doesn't appear:

Make sure you're on discord.com/quest-home
Refresh the page
Check that the extension is enabled in chrome://extensions/
Quest not completing:

Open the console (F12) and check for error messages
Make sure you've accepted the quests first
Some quest types work better in the actual Discord desktop app
Try refreshing and running the code again
User-Agent warnings:

The console might show warnings about user-agent detection - this is normal
The extension uses multiple methods to override it, so it should still work
Technical details
Built with Manifest V3. Uses:

declarativeNetRequest for header modification
Content scripts for quest page interaction
Background service worker for script injection
Webpack module interception for Discord internals
Concurrent execution with async/await and Promise.all
Mobile Version Supported (Android)
Download this Extension
Download Lemur Browser: Download Lemur Browser on Play Store
Open the browser and tap the 4 Squares Icon (on the right side) → select "Extensions".
Enable Developer mode, then tap + (from .zip/crx/.user.js) and upload the extension file you just downloaded.
Open the Discord Quests Page: Quest, accept at least one quest, select "Playing on Desktop", and then REFRESH.
A Running Quests button should appear. Tap it and you're all set!
If it doesn't appear, try refreshing the quest page again.
Notes: This setup is optimized for mobile via Lemur Browser because of its Chrome extension support.

Warning

This is a tool for automating Discord quests. Use at your own risk and be aware of Discord's Terms of Service. I'm not responsible if your account gets flagged or banned.

Important

This repository is strictly for educational purposes and security research only. It is designed to demonstrate how web APIs and user-agent spoofing work in a browser environment. Any misuse of this tool is the sole responsibility of the user. The author does not condone any actions that violate third-party Terms of Service.
