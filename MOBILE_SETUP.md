# Converting Your Compound Calculator to an iPhone App

## Why Capacitor?
✅ **Minimal code changes** — your existing HTML/CSS/JS works as-is  
✅ **Cross-platform** — one codebase for iOS and Android  
✅ **Native feel** — accesses phone hardware and App Store  
✅ **Easy maintenance** — update web code, sync to native apps  

## Step-by-Step Setup

### Prerequisites
- Node.js 16+ installed
- Xcode 14+ (for iOS development)
- An Apple Developer account (to publish)

### 1. Install Capacitor CLI
```bash
npm install -g @capacitor/cli
npm install
```

### 2. Initialize Capacitor
```bash
npx cap init
```
When prompted:
- **App Name**: `Compound Calculator`
- **App ID**: `com.compoundcalculator.app`
- **Web assets directory**: `www`

### 3. Create the Web Assets Folder
```bash
mkdir -p www
```

Move your HTML, CSS, and JS files into the `www/` folder:
- `www/index.html` — your main calculator HTML
- `www/css/` — your stylesheets
- `www/js/` — your JavaScript logic

### 4. Add iOS Platform
```bash
npx cap add ios
```

### 5. Build for iOS Development
```bash
npm run build:ios
```

### 6. Open Xcode
```bash
npx cap open ios
```

This opens your app in Xcode. You can now:
- Run on iOS Simulator
- Run on a physical device
- Make native tweaks if needed

### 7. Test in Simulator
In Xcode:
1. Select **iPhone Simulator** from the top dropdown
2. Click the **Play** button to build and run
3. Your calculator will appear in the simulator

### 8. Test on a Real Device
1. Connect your iPhone via USB
2. Select your device from the Xcode dropdown
3. Click **Play** to install and run

## Publishing to the App Store

### Requirements
- Apple Developer Account ($99/year)
- App screenshots, icons, description
- Privacy policy

### Steps
1. In Xcode: **Product** → **Scheme** → **Edit Scheme** → **Release**
2. **Product** → **Archive**
3. Upload via **Organizer** → **App Store Connect**

For detailed steps, see: [Apple Developer Guide](https://developer.apple.com/app-store/submissions/)

## Updating Your App

When you make changes to your calculator:

```bash
# Update web files (in www/ folder)
npm run sync        # Syncs changes to native projects
npm run build:ios   # Rebuild for iOS
npx cap open ios    # Open in Xcode to test
```

## Troubleshooting

### App won't load
- Check that `www/index.html` exists
- Open browser console in Xcode debugger for errors

### Can't find Xcode
- Install from App Store or [developer.apple.com](https://developer.apple.com)

### Build errors
- Run `npm install` to ensure all dependencies are installed
- Run `npx cap sync` to sync native code

## Next Steps
1. Organize your calculator files into the `www/` folder
2. Follow steps 1-6 above to get Xcode running
3. Test in the simulator
4. Deploy to App Store!

Need help? Let me know!
