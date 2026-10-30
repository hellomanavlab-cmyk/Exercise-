# Manav's Fitness & Grooming Hub

A lightweight personal website (HTML + CSS + JavaScript, no dependencies). Progress is saved in your browser with localStorage. Nothing is uploaded anywhere.

Files: `index.html`, `style.css`, `script.js`, `README.md`.

## Open it
Double-click `index.html`. It works offline, except the Google Drive video, which needs internet.

## Add / fix your Google Drive video
The video is already set in `script.js` (`VIDEO_ID` at the top) and plays through the Drive `/preview` URL.
1. Open the video in Google Drive, click **Share**.
2. Under General access choose **Anyone with the link** (Viewer).
3. If it still says access denied, or you want to swap the video, change `VIDEO_ID` in `script.js` (the part between `/d/` and `/view` in the Drive link), or send the video file separately so it can be hosted with the site.

### Timestamps (nothing is invented)
No timestamps are pre-filled because the video has not been analysed. To set them: watch the video, then open an exercise card and type the time in the **Video time** box (like `3:25`). It is saved in your browser, and **Show in video** will jump there. Drive's embedded player does not officially support start times, so if it starts at 0:00, drag the bar to the time shown.

## Test on your phone
- **Quick:** put the folder online (see below) and open the link on your phone.
- **Same Wi-Fi:** on your computer run `python3 -m http.server 8000` in this folder, find the computer's IP address, and open `http://<computer-ip>:8000` on your phone.
- Check: menu button, workout checklist, water and sleep trackers, video, and that data stays after a refresh.

## Publish online (free)
- **Netlify Drop:** go to app.netlify.com/drop and drag the folder in.
- **GitHub Pages:** create a repository, upload the 4 files, then Settings → Pages → deploy from `main`.
- **Cloudflare Pages:** create a project and upload the folder.

## Update later
Edit the files, then upload them again (Netlify: drag the folder again; GitHub: commit the changed files).
- Exercises: the `RAW` list in `script.js`.
- Workout days: `WO`, `SCHED`, `WARM`, `COOL`.
- Grooming, nutrition and sleep text: the `CARE` object.
- Colours: the `:root` variables in `style.css`.

## Limitations
- Progress is stored per browser and device and does not sync. Clearing browser data erases it.
- Stick-figure animations exist for 9 exercises (wall/knee/standard push-up, plank, squat, glute bridge, calf raise, wall sit, superman). Others use written steps.
- This is general wellness information, not medical advice. For pain, dizziness, skin problems or growth/weight worries, speak to a doctor.
