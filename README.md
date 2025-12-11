# Gatekeeper Plugins Marketplace

App store compliance checker plugins for Claude Code. Scan your apps and extensions for rejection risks before submission.

## Available Plugins

| Plugin | Platform | Description |
|--------|----------|-------------|
| **claude-ios-gatekeeper** | iOS / App Store | Scan for Apple App Store rejection risks |
| **claude-android-gatekeeper** | Android / Play Store | Scan for Google Play Store rejection risks |
| **claude-chrome-gatekeeper** | Chrome / Web Store | Scan for Chrome Web Store rejection risks |
| **claude-firefox-gatekeeper** | Firefox / AMO | Scan for Mozilla Add-ons rejection risks |

## Installation

### Step 1: Add the marketplace

```bash
/plugin marketplace add ophydami/gatekeeper-marketplace
```

### Step 2: Install plugins

```bash
# Install all four
/plugin install claude-ios-gatekeeper@gatekeeper-marketplace
/plugin install claude-android-gatekeeper@gatekeeper-marketplace
/plugin install claude-chrome-gatekeeper@gatekeeper-marketplace
/plugin install claude-firefox-gatekeeper@gatekeeper-marketplace

# Or install just the ones you need
/plugin install claude-ios-gatekeeper@gatekeeper-marketplace
```

## Usage

Each plugin provides:

| Command | Description |
|---------|-------------|
| `/[plugin]:scan` | Full compliance scan of your project |
| `/[plugin]:fix [issue]` | Fix a specific compliance issue |
| `/[plugin]:check-framework [name]` | Deep check for specific framework |

### Examples

```bash
# Scan iOS app for App Store issues
/ios-gatekeeper:scan

# Fix a specific Android issue
/android-gatekeeper:fix target-sdk-low

# Check Chrome extension with Plasmo
/chrome-gatekeeper:check-framework plasmo

# Scan Firefox extension for AMO compliance
/firefox-gatekeeper:scan
```

## Supported Frameworks

### iOS Gatekeeper
- Native Swift/Objective-C
- Expo
- React Native
- Flutter
- Capacitor
- Cordova
- Unity
- .NET MAUI

### Android Gatekeeper
- Native Kotlin/Java
- Expo
- React Native
- Flutter
- Capacitor
- Cordova
- Unity
- .NET MAUI

### Chrome Gatekeeper
- Vanilla JS/TS
- Plasmo
- WXT
- CRXJS/Vite
- React extensions
- Vue extensions

### Firefox Gatekeeper
- Vanilla JS/TS
- Plasmo
- WXT
- CRXJS/Vite
- React extensions
- Vue extensions
- Svelte extensions

## What Gets Checked

### iOS
- Privacy Manifest (PrivacyInfo.xcprivacy)
- Info.plist permissions and descriptions
- App Store Review Guidelines compliance
- Export compliance
- Entitlements configuration

### Android
- Target SDK version (API 35 for new apps, Aug 2025)
- Permission declarations and justifications
- Data Safety section readiness
- Play Store policy compliance
- Build and signing configuration

### Chrome
- Manifest V3 compliance
- Permission justification
- Content Security Policy
- Single purpose policy
- Remote code restrictions

### Firefox (Updated Nov 2025)
- data_collection_permissions manifest requirement
- browser_specific_settings.gecko configuration
- No remote code execution
- Source code reviewability
- Private browsing data handling
- User consent mechanisms

## Policy Sources

All plugins are kept up-to-date with the latest platform policies:

- **iOS**: [App Store Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)
- **Android**: [Google Play Policy Center](https://support.google.com/googleplay/android-developer/answer/11926878)
- **Chrome**: [Chrome Web Store Policies](https://developer.chrome.com/docs/webstore/program-policies/)
- **Firefox**: [Mozilla Add-on Policies](https://extensionworkshop.com/documentation/publish/add-on-policies/)

## License

MIT License - See individual plugin repos for details.

## Author

Gboyega Ofi (gboyega.ofi@gmail.com)
