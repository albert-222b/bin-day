# Bin Day — Merri-bek

A simple waste collection dashboard for Merri-bek City Council residents.

Shows upcoming bin collection dates for all 4 bins (general rubbish, FOGO, mixed recycling, glass) with a 6-week lookahead timeline.

## Setup — GitHub Pages (5 minutes)

### 1. Create a new repo

Go to [github.com/new](https://github.com/new) and create a repo called `bin-day` (or whatever you like). Make it **public**.

### 2. Push the files

```bash
git init
git add index.html manifest.json
git commit -m "Initial commit"
git branch -M main
git remote add origin git@github.com:YOUR_USERNAME/bin-day.git
git push -u origin main
```

### 3. Enable GitHub Pages

- Go to your repo → **Settings** → **Pages**
- Under "Source", select **Deploy from a branch**
- Branch: **main**, folder: **/ (root)**
- Click **Save**
- Your site will be live at `https://YOUR_USERNAME.github.io/bin-day/` in about a minute

### 4. Add to your phone home screen

- Open the URL in Chrome on your Pixel 9
- Tap the **⋮** menu → **Add to Home screen**
- It'll appear as "Bin Day" with a bin emoji icon

### 5. First-time setup

The app will ask you to enter:
- Your address
- Your collection day (Monday–Friday)
- Your next recycling date (yellow lid)
- Your next glass date (purple lid)

Find these details on the [council waste calendar](https://www.merri-bek.vic.gov.au/waste-calendar26/).

Settings are saved in your browser's localStorage and persist across visits.

## Wednesday reminders

For push notifications on your phone every Wednesday at 7pm, import the `bin-reminders.ics` file into Google Calendar. Each event lists which bins to put out that night.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire app — single self-contained file, no build step |
| `manifest.json` | PWA manifest for home screen install |
| `bin-reminders.ics` | Calendar events with Wed 7pm reminders (optional) |

## Notes

- Works offline after first load (all logic is client-side)
- No API calls — schedule is calculated from your configured dates
- No tracking, no cookies, no external services (apart from Google Fonts)
- Public holidays with no collection: Christmas, New Year's, Good Friday, Anzac Day
