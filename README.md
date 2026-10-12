# Block by Block

A personal habit tracker where finishing daily tasks earns coins, and coins build your city.
No accounts, no servers, no tracking: everything is stored on your own device.

## Files
- `index.html`: the whole app
- `manifest.webmanifest`, `sw.js`, `*.png`: make it installable on a phone and usable offline

## Run it on your computer (30 seconds)
The app needs to be served over `http://localhost` (double-clicking the file works for the app itself, but the offline/install features need a server).

Pick whichever you have:

    cd block-by-block
    python3 -m http.server 8000      # Python
    # or
    npx serve .                      # Node

Then open http://localhost:8000

## Put it on your phone (GitHub Pages, free)
1. Create a free account at github.com and click **New repository**. Name it `block-by-block`. Public is fine, because the code holds none of your personal data (your answers live in your browser).
2. Click **uploading an existing file**, drag in every file from this folder, and commit.
3. Go to **Settings > Pages**. Under "Build and deployment" choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and Save.
4. After a minute your app is live at `https://YOUR-USERNAME.github.io/block-by-block/`
5. Open that link on your phone:
   - **iPhone (Safari):** Share button > Add to Home Screen
   - **Android (Chrome):** menu (⋮) > Install app / Add to Home screen. On Xiaomi/Poco phones use **Chrome**, not the built-in Mi Browser, which handles installs poorly.

It then opens full screen like a normal app and works offline.

## Good to know
- **Data is per device.** Your phone and your laptop have separate cities. To move one to the other, use **You > Export backup** on one and **Import backup** on the other. Do this now and then as a backup too.
- **Updating the app:** after you change `index.html`, edit `VERSION` in `sw.js` (for example `bbb-v2`) before you commit. That makes phones fetch the new version.
- **Clearing browser/site data deletes your city**, so export a backup first.

## How it works
- About 30 to 40 questions at the start (more or fewer, depending on which life areas you pick) generate your task list.
- Each day it picks a mix that fits your time, energy, difficulty and weekend preferences. You tell it your energy each morning.
- Tap a task to complete it and earn coins. Finish everything for a perfect-day bonus that grows with your streak.
- Spend coins on the City tab. Your level rises as you earn, and unlocks bigger buildings.
- A "question of the day" asks one more thing about you per day. Some answers can become tasks.
- Change any answer in **You**, and your tasks update immediately.
