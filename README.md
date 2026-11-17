# Saida's workouts

A small offline web app: a guided home exercise session, animated figures for each
exercise, English and Malayalam, and a tracker that stays on the phone.

## Files

- `index.html` – the whole app (pages, styles, exercises, figures)
- `sw.js` – makes the app work offline
- `manifest.webmanifest`, `icon-*.png` – lets Android install it on the home screen

## What is in the app

- Today: the day's session with one large Start button, the week at a glance,
  and a count of active weeks (weeks with 2 or more sessions).
- Session: one exercise per screen with "Exercise 3 of 13", a figure she can
  pause, slow down or replay, a one-line instruction, and a circle to tap for
  counting or timing. The phone vibrates and beeps when a timer ends.
- Check-in: five pain faces (saved as 0, 2, 5, 8 or 10) before and after.
- Flare-day mode: one tap on Today hides the normal plan and leaves only the
  gentle 5-minute routine until she switches it off.
- Progress: weekly summary with "Send to family", ribbons, calendar, charts,
  and a one-page report for the doctor (4 or 8 weeks, in English).
- Settings: language, light or dark colours (automatic in the evening),
  vibration and beep, slow-motion figures, reminders, backup.

## Put it on GitHub Pages

1. Create a new repository on GitHub. Give it a name that is hard to guess,
   for example `sw-7f3k9q2x`. The site address will be
   `https://YOUR-USERNAME.github.io/REPO-NAME/`.
2. Upload all the files in this folder to the repository (Add file → Upload files).
3. Open Settings → Pages. Under "Build and deployment" choose
   Source: "Deploy from a branch", Branch: `main`, folder `/ (root)`, then Save.
4. Wait a minute or two, then open the site address.

## Install on the Android phone

1. Open the site address in Chrome on her phone.
2. Tap the three-dot menu → "Add to Home screen" (or "Install app").
3. Open it once from the home screen while online. After that it works offline.

## Privacy

- Sessions, pain scores and notes are stored only in the phone's browser.
  Nothing is sent to GitHub or anywhere else.
- A GitHub Pages site can be opened by anyone who has its address. GitHub does
  not offer a password or sign-in for Pages on personal accounts. The page asks
  search engines not to list it, and a hard-to-guess repository name keeps the
  address private in practice, but treat the address like a key.
- The site itself contains the exercise plan, the title and the first name
  "Shahida". It contains no health records.
- Family see progress only when she taps "Send to family" on the Progress
  page. That sends a short weekly summary and a link holding a read-only
  snapshot. Her notes are never included. The snapshot
  sits after the `#` in the link, which browsers never send to the server.
  Anyone who is given that link can see the snapshot, so send it only to family.

## Changing things

- All exercise text (both languages), doses and video links are near the top of
  the script in `index.html`, in the block that starts with `const V = {`.
- After any change, raise the version in `sw.js` (now `saida-workouts-v2`, so
  next time `v3`) so phones pick up the new files.
- To update a site that is already on GitHub: open the repository, choose
  Add file → Upload files, drop in all the files from this folder and commit.
  They replace the old ones. On the phone, open the app twice while online:
  the first opening downloads the update, the second one shows it. Her record
  on the phone is kept.
- Backups: Settings → "Save backup file". Do this now and then, because clearing
  Chrome's data or changing phone removes the record.
