# Capsule Reader prototype

A clickable prototype of the Capsule Reader app for GI doctors. One link works everywhere:

| You open the link on | You get |
|---|---|
| A phone or tablet | The phone app, full screen (`index.html`) |
| A computer with a mouse | The desktop prototype, scaled to your window (`desktop.html`) |
| Any device, with `#phone` on the end of the link | The phone app, even on a computer |
| `sizes.html` | Every device from a 320 px phone to a 1440 px desktop, at every text size |

All names and cases in the prototype are made up. The frames are de-identified.

---

## Put it online (once, about 5 minutes)

1. **Make the repository.** On github.com, click **+** (top right), then **New repository**.
   - Name: `capsule-reader`
   - Visibility: **Public**. Free GitHub accounts can only publish Pages from public repositories.
   - Leave "Add a README" unticked, then click **Create repository**.
2. **Upload the files.** On the empty repository page, click **uploading an existing file**. Drag in everything from this folder, including the `icons` and `video` folders, then click **Commit changes**.
   - The `.nojekyll` file starts with a dot, so your computer may hide it. It is optional; the site works without it.
3. **Turn on Pages.** Go to **Settings**, then **Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, Branch to **main**, folder **/ (root)**, then **Save**.
4. **Wait a minute.** Refresh the Pages settings. Your link appears at the top, for example:
   `https://YOUR-USERNAME.github.io/capsule-reader/`

## Put it on your phone like an app

- **iPhone or iPad:** open the link in **Safari**, tap **Share**, then **Add to Home Screen**. Open it from the new icon: it runs full screen, with no address bar.
- **Android:** open the link in **Chrome**, tap **⋮**, then **Install app** (or **Add to Home screen**).

After the first open it also works offline.

## Change something later

- **Small edit:** open the file on github.com, click the pencil, edit, then **Commit changes**. The site updates in about a minute.
- **Replace a file:** in the folder, click **Add file**, then **Upload files**, and drop in the new version with the same name.
- **Phone still shows the old version?** Close the app fully and open it again. If it still sticks, open `sw.js`, change `capsule-reader-v1` to `capsule-reader-v2`, and commit.

## Try it on your computer first (optional)

In this folder, run:

```
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser. To see the phone app on a computer, open `http://localhost:8000/#phone`.

## What is in here

| File | What it is |
|---|---|
| `index.html` + `assets/` | The phone prototype, exactly the Round 20 design: Patients, Community, Insights, menu, notifications, a case (rail and wheel, panels, command bar, pencil, hold to pin or comment) and the report. |
| `desktop.html` + `support.js` | The desktop prototype. `support.js` is the runtime it needs. |
| `sizes.html` | An earlier responsive sketch for checking text sizes; not the final design. |
| `manifest.webmanifest`, `icons/` | What makes "Add to Home Screen" open full screen with the right icon. |
| `sw.js` | Keeps it working offline and picks up your changes. |
| `video/` | Where the real capsule clip goes later. Read `video/README.md` first. |
