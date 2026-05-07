# Planetek BD Dashboard — Setup Guide
## Africa & Middle East Business Development

---

## What you need (all free)
- A **GitHub account** ✅ you have this
- A **Google account / Gmail** ✅ you have this
- Chrome or Edge browser (recommended)

---

## STEP 1 — Upload to GitHub Pages

### 1.1 — Create a new repository
1. Go to **github.com** → log in
2. Click **+** (top right) → **New repository**
3. Name: `planetek-bd`
4. Visibility: **Public**
5. Click **Create repository**

### 1.2 — Upload the files
1. On the new repo page → **Add file** → **Upload files**
2. Upload ALL four files from this folder:
   - `index.html`
   - `manifest.json`
   - `icon-192.png`
   - `icon-512.png`
3. Click **Commit changes**

### 1.3 — Enable GitHub Pages
1. Repo → **Settings** tab → **Pages** (left sidebar)
2. Source: **Deploy from a branch**
3. Branch: **main** | Folder: **/ (root)** → **Save**
4. Wait 3 minutes. Your URL will appear:
   ```
   https://YOUR-GITHUB-USERNAME.github.io/planetek-bd
   ```
5. ✅ Send this URL to Ahmed. That's all he needs.

---

## STEP 2 — Set up Firebase (real-time sync)

### 2.1 — Create Firebase project
1. Go to **console.firebase.google.com**
2. **Add project** → Name: `planetek-bd`
3. Disable Google Analytics → **Create project** → **Continue**

### 2.2 — Create Realtime Database
1. Left sidebar → **Build** → **Realtime Database**
2. **Create Database**
3. Location: **Europe (Belgium)** (closest to Italy)
4. Mode: **Test mode** → **Enable**
5. Copy your database URL — looks like:
   ```
   https://planetek-bd-xxxxx-default-rtdb.europe-west1.firebasedatabase.app
   ```
   ← **Save this URL. You will paste it into the dashboard.**

### 2.3 — Set database rules
1. Click **Rules** tab
2. Replace all content with:
   ```json
   {
     "rules": {
       ".read": true,
       ".write": true
     }
   }
   ```
3. Click **Publish**

---

## STEP 3 — First launch

1. Open: `https://YOUR-USERNAME.github.io/planetek-bd`
2. Setup screen appears — fill in:
   - **Who are you?** → Click **Gamal**
   - **Firebase URL** → paste from Step 2.2
3. Click **Launch Dashboard** ✅

### For Ahmed:
1. Send him the same URL
2. He clicks **Ahmed** → pastes same Firebase URL → Launch
3. ✅ Both of you are now synced live

---

## STEP 4 — Install as an app (optional)

### Laptop — Chrome or Edge:
- Look for install icon in address bar → click → **Install**
- App appears on your desktop

### Android phone:
- Chrome → 3-dot menu → **Add to Home screen**

### iPhone:
- Safari → Share button → **Add to Home Screen**

---

## STEP 5 — Update dashboard in future

When you get a new `index.html` from me:
1. GitHub repo → click `index.html` → pencil icon (Edit)
2. Select all → Delete → Paste new content
3. **Commit changes**
4. Wait 3 minutes → refresh URL → done ✅

---

## Troubleshooting

| Problem | Fix |
|---------|-----|
| Page not loading | Wait 5 min after first upload |
| Data not syncing | Check Firebase URL — no trailing slash |
| Changes not showing | Ctrl+Shift+R to hard refresh |
| Permission denied | Redo Step 2.3 (Rules = true) |
| Can't install app | Use Chrome or Edge, not Firefox |

---

## Your details (fill in after setup)

**Dashboard URL:**
`https://_______________________.github.io/planetek-bd`

**Firebase URL:**
`https://_______________________.firebasedatabase.app`

---
*Need help with any step? Paste the error to Claude.*
