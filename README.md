# Site Photo Checklist

A simple, phone-friendly web app. Pick a **Mount type** and it shows only the photos/measurements needed for that mount.

| Mount type  | Checklist items                          |
|-------------|------------------------------------------|
| Ballast     | Level pic, Height pic                    |
| Nano        | Whip length, Level pic, Pipe length      |
| Sleeve wall | Sleeve length, Bracket separation        |
| Timber      | Stud size, Stud separation               |

## Features
- Mount type dropdown → filtered checklist
- Tick items off, with a progress bar
- "Add photo" opens the phone camera; adding a photo ticks the item automatically
- Notes / measurement field per item
- "Download photos" saves them named `Site_Mount_Item_1.jpg`
- Checks and notes are remembered on the device (photos stay until the page is closed)

## Put it on GitHub Pages
1. Create a new repository on GitHub (e.g. `site-photo-checklist`).
2. Upload `index.html` and `README.md` (**Add file → Upload files**), then commit.
3. Go to **Settings → Pages**, set **Source** to *Deploy from a branch*, branch `main`, folder `/ (root)`, and save.
4. After a minute your app is live at `https://<your-username>.github.io/site-photo-checklist/`.

## Editing the checklist
Open `index.html` and edit the `CHECKLISTS` block near the top of the script:

```js
const CHECKLISTS = {
  "Ballast":     ["Level pic", "Height pic"],
  "Nano":        ["Whip length", "Level pic", "Pipe length"],
  "Sleeve wall": ["Sleeve length", "Bracket separation"],
  "Timber":      ["Stud size", "Stud separation"]
};
```

Add a new line for a new mount type, or add/remove items inside the brackets.
