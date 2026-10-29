# Plate & Pace Run

Run plan + GPS run tracker with a voice coach, for iPhone.
Everything stays on your phone (no account, no server).

## Put it on your iPhone (about 10 minutes, once)

GPS only works on a secure (https) web address, so the app needs to be hosted.
GitHub Pages does this for free.

1. Sign in at github.com and create a new repository, e.g. `pace` (Public).
2. Click **Add file → Upload files** and drop in everything from this folder:
   `index.html`, `sw.js`, `manifest.webmanifest`, `icon-180.png`, `icon-192.png`, `icon-512.png`. Commit.
3. Go to **Settings → Pages**. Under "Build and deployment" choose **Deploy from a branch**,
   branch `main`, folder `/ (root)`, then Save.
4. After a minute your app is live at `https://<your-username>.github.io/pace/`.
5. Open that address in **Safari** on your iPhone → Share button → **Add to Home Screen**.
6. Open **Pace** from the home screen and tap Start on any run once, so iOS asks for location.
   Choose **Allow While Using App**.
   If you ever blocked it: Settings › Privacy & Security › Location Services › Safari Websites →
   While Using the App, Precise Location on.

## Before a run

- Turn the ringer/silent switch so you can hear it, or wear headphones.
  Music keeps playing; the voice speaks over it.
- Set **Settings › Display & Brightness › Auto-Lock** to a long time or Never during the run.
  iOS pauses web apps when the screen locks: the clock keeps counting and the route is joined up
  when you unlock, but you won't get voice cues while it's locked.
  The app also asks the phone to keep the screen awake on its own.
- Wait for the GPS dot to turn green, then Start.
- Ending a run needs a 1-second press on **Hold to end**, so a bump can't stop it.
- If the app gets closed mid-run, reopen it and choose **Continue it**.

## What it says

- Each block as it starts (warm-up, rep with target pace, recovery, cool-down).
- During reps: pace check every 30 s ("Pick it up / Ease off / On pace"),
  halfway on long reps, "100 meters" near the end, then your rep time and pace.
- During steady running: a pace check every 2 minutes, plus kilometre splits.
- Beeps on the last 3 seconds of timed blocks.

## Updating the app

Replace `index.html` in the repository. Also change `VERSION` in `sw.js`
(e.g. `pace-v2`) so the phone picks up the new version. Close and reopen the app twice.

## Backup

Settings › Export backup saves a file with all runs; Import restores it.
Do this occasionally; deleting the home-screen app deletes its data.

## Try it at home

Open `…/pace/?sim=10` to run a simulated GPS run at 10× speed and hear the cues.
Runs from simulation mode are saved like real ones, so delete them afterwards.
