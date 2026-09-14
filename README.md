# ⚡ ZALDO — Finance Redefined
> **Premium Personal Wealth Companion & Automated Financial Tracker**  
> *Powered by Ninetech*

[![Version](https://img.shields.io/badge/Release-v1.0.1-brightgreen.svg)](https://github.com/anwar0085/zaldo/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Android-0F1211.svg?logo=android)](https://developer.android.com/)
[![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack%20Compose-4285F4.svg?logo=jetpackcompose)](https://developer.android.com/jetpack/compose)
[![Architecture](https://img.shields.io/badge/Security-Zero--Knowledge%20Encrypted-90CCA3.svg)](#security--privacy)

---

## 🌟 Overview

**ZALDO** is a state-of-the-art Android personal finance application crafted with geometric elegance, high-density precision, and privacy-first architecture. It automates expense tracking, receipt processing, subscription monitoring, and financial statement generation without compromising user privacy.

---

## 🚀 Key Features

### 1. 🤖 Zero-Touch Financial Automation
- **Smart SMS & Notification Engine**: Parses transactional SMS and bank notification payloads locally in real-time.
- **Privacy-First Processing**: Personal SMS and OTPs are ignored via deterministic regex filtering; financial metadata stays on device.
- **Duplicate & Replay Protection**: Cryptographic hashing of transaction strings prevents duplicate entries.

### 2. 📷 Deterministic Financial OCR Engine
- **Multi-Pass Structural & Geometric Parsing**: Extracts structured transactional metadata with high precision across Indian financial apps (Navi UPI, BHIM, CRED, PhonePe, Paytm, Amazon Pay, GPay).
- **UPI Handle & VPA Sanitization**: Pre-scrubs account numbers and UPI handles to eliminate noise during amount identification.
- **Hero Amount Dominance**: Identifies transaction amounts using font height dominance and two-token currency pairing.

### 3. 🎙️ Voice AI Transaction Logger
- **Real-Time Speech Processing**: Powered by continuous speech recognition with live transcription previews.
- **Natural Language Parsing**: Translates spoken financial prompts (e.g. *"Paid 450 rupees for dinner at Swiggy via HDFC"*) into categorized transaction drafts.

### 4. 🔒 Biometric Security & Autopay Vault
- **Biometric App Lock**: Supports Fingerprint, Face ID, and Device Credential fallback with background inactivity auto-lock.
- **Autopay & Split UPI Card**: Encrypted local storage for recurring mandate cards and split bills, synchronized securely with Cloud Firestore.
- **Encrypted Local Database**: Room database storing financial ledger entries locally on disk.

### 5. 📄 Bank-Grade Statement Generator
- **PDF Export Engine**: Generates PDF account statements complete with transaction breakdowns, category summaries, and official Zaldo branding.

### 6. 🔄 Integrated In-App Update Engine
- **One-Tap Over-the-Air Updates**: Direct integration with GitHub Releases & Firebase Firestore configuration (`app_config/app_update`).
- **Seamless Downloader**: Checks, alerts, downloads, and prompts installation right within the app.

---

## 🛠️ Tech Stack & Architecture

| Layer | Technology |
|---|---|
| **Language** | Kotlin 2.2 |
| **UI Framework** | Jetpack Compose + Material 3 |
| **Local Database** | AndroidX Room (KSP Code Generation) |
| **Asynchronous Engine** | Kotlin Coroutines & Reactive StateFlow |
| **Local Preferences** | Jetpack DataStore Preferences |
| **Vision & ML** | Google ML Kit Text Recognition |
| **Barcode/QR** | ZXing Core Engine |
| **Cloud & Auth** | Firebase Auth, Google Credential Manager, Cloud Firestore |
| **Splash Engine** | AndroidX Core SplashScreen API |

---

## 📥 Installation & Updating

1. Download the latest **`zaldo-release.apk`** from the [Releases](https://github.com/anwar0085/zaldo/releases/latest) tab.
2. Open the downloaded `.apk` file on your Android device.
3. Allow *"Install unknown apps"* if prompted by your browser or file manager.
4. Launch **Zaldo** to experience finance redefined.
5. Subsequent updates can be downloaded directly from the **Profile > Check for Updates** section inside the app.

---

## ⚙️ Building from Source

```bash
# Clone the repository
git clone https://github.com/anwar0085/zaldo.git
cd zaldo

# Compile and verify Kotlin sources
./gradlew compileDebugKotlin

# Build Debug APK
./gradlew assembleDebug

# Build Production Release APK
./gradlew assembleRelease
```

---

## 📄 License & Attribution

Designed and engineered for **ZALDO**.  
*Powered by Ninetech. All rights reserved.*
