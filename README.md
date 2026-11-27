# SMaxx CAD Assistant

An offline jewellery CAD studio in one web page. It needs no API keys, no Claude and no server.

- **Fix**: answers for common CAD and casting problems (Rhino, Matrix, ZBrush, Magics, KeyShot)
- **Learn**: software mastery hub with progress tracking
- **Calculate**: tolerances, metal weight, quotes, ring and diamond sizes, jobs list
- **Make**: step-by-step build guides
- **Practice**: daily log, design briefs and a work reviewer
- **Discover**: upload images, renders, GIFs or videos, type one line such as
  `Jhumka pink stones pearl drop 18k Matrix 9 45x18mm vol 1028.9`,
  and the item details fill in automatically (name, ID, size, Matrix 9 weight, stones, description).
  Save items to Catalogue, Practice, Reference or Scrapped.

## Put it on GitHub Pages

1. Create a new repository on GitHub, for example `smaxx-cad-assistant`.
2. Upload **everything inside this folder** to the repository root
   (`index.html`, `sw.js`, `manifest.webmanifest`, `logo.png`, `logo-wide.png`, `icons/`, `.nojekyll`).
   On the web, use **Add file → Upload files** and drag the files and the `icons` folder in.
3. Go to **Settings → Pages**. Under *Build and deployment*, choose **Deploy from a branch**,
   pick `main` and `/ (root)`, then **Save**.
4. After 1–2 minutes the app is live at `https://YOUR-NAME.github.io/smaxx-cad-assistant/`.

> On a free GitHub plan, Pages needs a **public** repository. People can open the page,
> but they can't see your saved items, because those stay in your own browser.

## Install it as an app

Open the GitHub Pages link, then tap **📲 Install app** on the Home screen (or in the side menu).

- **Android (Chrome):** the install prompt opens directly, or use menu ⋮ → *Install app*.
- **iPhone / iPad (Safari):** Share → *Add to Home Screen*.
- **Windows / Mac (Chrome or Edge):** the install icon in the address bar.

After the first visit the app works **fully offline**.

## Your data

- Everything is saved in the browser on that device (localStorage and IndexedDB for media).
- Different devices and different web addresses keep separate data.
  Use **Save backup** (it includes Discover photos and videos) and **Load backup** to move data.
- Export a backup regularly. Clearing browser data deletes your items.

## Update the app

Upload the new `index.html` over the old one. Your saved data is kept.
If you change other files, also change `VERSION` at the top of `sw.js` (for example `smaxx-v2`)
so installed copies download the new files.

## Open without GitHub

You can also open `index.html` straight from your computer. Everything works,
except installing as an app, which needs an `https://` address.

## v1.1 changes

- Slim header strip on Home; the app icon inside it is full size (fills its square edge to edge).
- `index.html` is now fully self-contained: icons are embedded, and it builds its own web manifest when no manifest file is reachable.
- Install button: native prompt when the browser offers it, otherwise a 2-step modal (menu ⋮ / Share → Add to Home Screen / Install app).
  Installing is blocked inside preview frames and local files; open the https link in its own tab.
  Upload `sw.js` together with `index.html` on hosting: browsers refuse service workers made from inline blobs.
- Discover: new offline naming engine (3 words max, e.g. `Crimson Lotus _Jhumka`, ID `CL_J`), no repeated names (remembered in localStorage), and a 🎲 Shuffle Name button.
