# Gatekeeper Plugins Marketplace

App store compliance checker plugins for Claude Code. Scan your apps and extensions for rejection risks before submission.

## Available Plugins

| Plugin | Platform | Description |
|--------|----------|-------------|
| **claude-ios-gatekeeper** | iOS / App Store | Scan for Apple App Store rejection risks |
| **claude-android-gatekeeper** | Android / Play Store | Scan for Google Play Store rejection risks |
| **claude-chrome-gatekeeper** | Chrome / Web Store | Scan for Chrome Web Store rejection risks |

## Installation

### Step 1: Add the marketplace

```bash
/plugin marketplace add ophydami/gatekeeper-marketplace
```

### Step 2: Install plugins

```bash
# Install all three
/plugin install claude-ios-gatekeeper@gatekeeper-marketplace
/plugin install claude-android-gatekeeper@gatekeeper-marketplace
/plugin install claude-chrome-gatekeeper@gatekeeper-marketplace

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

## What Gets Checked

### iOS
- Privacy Manifest (PrivacyInfo.xcprivacy)
- Info.plist permissions and descriptions
- App Store Review Guidelines compliance
- Export compliance
- Entitlements configuration

### Android
- Target SDK version (API 34+)
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

## License

MIT License - See individual plugin repos for details.

## Author

Gboyega Ofi (gboyega.ofi@gmail.com)
