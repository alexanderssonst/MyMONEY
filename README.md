# MyMONEY: offline budget app

Monthly income, split into Needs / Wants / Savings (Liquid + Invested), with a selectable budget rule (50/30/20, 60/20/20, 70/20/10 or custom). It logs every purchase, learns your frequent items, repeats fixed costs every month, and gives you a Recap with money-saving tips. Everything is stored and calculated on the device, and the app works with no connection once installed.

## Files

```
index.html             the whole app (layout, styles, logic, Recap engine, EN/IT texts)
manifest.webmanifest   makes it installable
sw.js                  service worker: offline cache
.nojekyll              tells GitHub Pages to serve the files as they are
icons/                 home-screen icons
logo/piggy.svg         the logo
fonts/                 Onest font (SIL Open Font License, see OFL-LICENSE.txt)
```

## Upload to GitHub Pages (free)

iPhone installs web apps only from an `https://` address. After the first install the app never needs internet again.

1. Create a free account on github.com, then a **new repository** (for example `mymoney`), set to **Public**.
2. Unzip `budget-app.zip`. Click **Add file → Upload files** and drag in everything *inside* the `budget-app` folder: `index.html`, `sw.js`, `manifest.webmanifest`, `.nojekyll`, `README.md` and the `icons`, `fonts` and `logo` folders. Click **Commit changes**.
   - `.nojekyll` is a hidden file. On a Mac, press **Cmd + Shift + .** in Finder to show it. If it doesn't get uploaded, the app still works.
3. Go to **Settings → Pages**. Under *Source* choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
4. After a minute or two the link appears on that page: `https://<your-username>.github.io/mymoney/`

A Public repository means anyone with the link can open the empty app page. Your data never leaves your phone.

## Install on iPhone

1. Open the link in **Safari**.
2. Tap **Share → Add to Home Screen → Add**.
3. Open it once from the new icon while still online, so everything gets saved for offline use.

## Desktop

Open the same link in Chrome or Edge and click the install icon in the address bar.

## Using the app

- **Add:** the **+ Add** button at the bottom of each card.
- **Quick add:** the chips above the button are your most-used items with their last amount. Tap one, confirm the amount, done.
- **Repeated purchases** stack into one row (for example *Gas ×3*). Tap it to see each entry.
- **Repeats every month:** switch it on for fixed costs or salary. They appear by themselves in each new month.
- **Icons** are picked from the name (English or Italian). Tap the icon in the add sheet to choose another.
- **Edit:** tap a row. **Delete:** swipe a row left, or use Delete in the edit sheet.
- **Change month:** swipe left/right on the page or use the arrows. Tap the month name to go back to the current month.
- **Recap:** insights and tips calculated on the phone (spending pace, items that add up, unusual increases, savings rate, recurring costs, months in a row within your rule). On the last days of a month it adds a short summary.
- **Savings:** this month's Liquid and Invested, plus the **total saved** up to the month you're viewing.
- **Settings:** save file, budget rule, language (English/Italiano), theme (Dark/Light/Auto), colors (Colorful/Monotone), style (Liquid Glass/Solid), font (Onest/System), currency, reset.
- **Backup reminder:** a gold dot on the settings button means you haven't exported in 14 days.

## Save file

Settings → **Export** creates `mymoney-save-YYYY-MM-DD.json`. On iPhone the share sheet opens: choose *Save to Files*, iCloud Drive or AirDrop. On desktop it goes to Downloads.

Settings → **Import** loads a save file and **replaces** the data on that device. Older save files still import.

Data on one device is never shared automatically with another, so export regularly. On iPhone, deleting the home-screen icon also deletes its data.

## Updating the app

Upload the new files to the same repository, replacing the old ones. Then open the app twice while online: the first launch downloads the update, the second shows it.

## Notes

- Switching between Light and Dark changes the iPhone status bar colors the next time the app is opened from the home screen.
- If *Reduce Transparency* is on in iOS accessibility settings, the Solid style is used automatically.
