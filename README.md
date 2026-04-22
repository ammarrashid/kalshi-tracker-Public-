# Kalshi Promo Tracker

A private, mobile-first PWA to track Kalshi promotional quote payments across two accounts.

**Accounts:** `@maira4yo` ($50/quote) · `@stfnigg` ($40/quote)

---

## 🚀 Deploy to GitHub Pages (Step by Step)

### Step 1 — Create a GitHub account
Go to [github.com](https://github.com) and sign up if you don't have an account.

### Step 2 — Create a new repository
1. Click the **+** icon (top right) → **New repository**
2. Name it: `kalshi-tracker`
3. Set it to **Public** *(required for free GitHub Pages)*
4. Click **Create repository**

### Step 3 — Upload the files
1. On your new repo page, click **uploading an existing file**
2. Drag and drop ALL these files at once:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon.png`
3. Scroll down, click **Commit changes**

### Step 4 — Enable GitHub Pages
1. Go to your repo → **Settings** tab
2. Scroll down to **Pages** (left sidebar)
3. Under **Source**, select **Deploy from a branch**
4. Branch: **main** · Folder: **/ (root)**
5. Click **Save**

### Step 5 — Get your live URL
- Wait ~60 seconds, then refresh the Settings > Pages page
- Your app will be live at:
  ```
  https://YOUR-USERNAME.github.io/kalshi-tracker/
  ```

---

## 📱 Install on iPhone (Add to Home Screen)

1. Open the live URL in **Safari**
2. Tap the **Share** button (box with arrow)
3. Tap **Add to Home Screen**
4. Tap **Add**

The app will now appear on your home screen and work offline like a native app.

---

## Features

- ✅ Dual account tracking — @maira4yo & @stfnigg
- ✅ Status slider per entry — Paid / Pending / Not Invoiced
- ✅ Summary cards with live totals
- ✅ Progress bar breakdown
- ✅ Add & delete entries daily
- ✅ Filter by account or status
- ✅ Data saved locally on your device (IndexedDB)
- ✅ Works offline (Service Worker)
- ✅ Installable as PWA on iOS & Android

---

## Data & Privacy

All data is stored **locally on your device** using IndexedDB.  
No data is sent to any server. Fully private.

---

## Update Numbers

To update the starting quote counts, open `index.html`, find the `seed()` function and edit the `mk(...)` lines:

```js
mk(33, 'maira',   'paid',       80, 2);  // 33 paid quotes
mk(11, 'maira',   'pending',    12, 2);  // 11 invoice pending
mk(5,  'maira',   'uninvoiced',  0, 1);  // 5 not invoiced
mk(4,  'stfnigg', 'pending',     8, 2);  // 4 invoice pending
mk(7,  'stfnigg', 'uninvoiced',  0, 1);  // 7 not invoiced
```

Then increment `const VER = 6` to `const VER = 7` so the app reloads fresh data.

After editing, re-upload `index.html` to GitHub and the live site updates automatically.
