# NS Photography - Android App

A WebView wrapper that turns the NS Photography web app into an Android application.

## Setup Instructions

### Step 1: Update the App URL

Open `App.tsx` and replace `YOUR-REPLIT-APP-URL` with your actual deployed Replit app URL:

```typescript
const APP_URL = "https://your-app-name.replit.app";
```

### Step 2: Create an Expo Account

1. Go to [expo.dev](https://expo.dev) and create a free account
2. Generate an access token at [expo.dev/accounts/settings/access-tokens](https://expo.dev/accounts/settings/access-tokens)

### Step 3: Push to GitHub

1. Create a new GitHub repository
2. Push this folder to the repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

### Step 4: Add GitHub Secret

1. Go to your GitHub repo → Settings → Secrets and Variables → Actions
2. Add a new secret named `EXPO_TOKEN` with your Expo access token

### Step 5: Build the APK

**Option A: GitHub Actions (Automatic)**
- Push to `main` branch or go to Actions tab → "Build Android APK" → Run workflow
- The build will start on Expo's servers

**Option B: Local Build**
```bash
npm install
npx eas login
npx eas build --platform android --profile preview
```

### Step 6: Download APK

1. Go to your [Expo dashboard](https://expo.dev)
2. Find the completed build under your project
3. Download the APK file
4. Install on your Android device

## Project Structure

```
├── App.tsx                    # Main app with WebView
├── app.json                   # Expo configuration
├── eas.json                   # EAS Build profiles
├── package.json               # Dependencies
├── assets/                    # App icon and splash screen
└── .github/workflows/         # GitHub Actions for auto-build
```

## Customization

- **App Icon**: Replace `assets/app-icon.png` (1024x1024 recommended)
- **Splash Screen**: Replace `assets/splash.png` (1284x2778 recommended)
- **Package Name**: Change `com.nsphotography.invoice` in `app.json`
- **Colors**: Update the brown/gold hex values in `App.tsx` and `app.json`
