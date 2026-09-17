# ⚡ ZALDO — Finance Redefined
> **Premium Personal Wealth Companion & Automated Financial Intelligence Platform**  
> *Engineered by Ninetech*

[![Version](https://img.shields.io/badge/Release-v1.0.3-brightgreen.svg)](https://ninetech.cloud/zaldo/zaldo.apk)
[![Platform](https://img.shields.io/badge/Platform-Android-0F1211.svg?logo=android)](https://developer.android.com/)
[![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack%20Compose-4285F4.svg?logo=jetpackcompose)](https://developer.android.com/jetpack/compose)
[![Security](https://img.shields.io/badge/Security-Zero--Knowledge%20Encrypted-90CCA3.svg)](#-security--privacy-architecture)
[![License](https://img.shields.io/badge/License-Proprietary-orange.svg)](#-license--attribution)

---

## 🌟 Overview

**ZALDO** is an elite Android personal finance and automated wealth intelligence platform crafted with dark aesthetic elegance, high-density financial ergonomics, and a strict privacy-first architecture. 

It automates everyday expense tracking, bank receipt OCR scanning, voice logging, autopay mandate monitoring, network referral tracking, and professional financial statement generation without ever exposing sensitive credentials.

---

## 📥 Direct Download & Installation

The fastest way to install or update Zaldo on your Android device:

👉 **[Download Latest APK (v1.0.3)](https://ninetech.cloud/zaldo/zaldo.apk)**

1. Download `zaldo.apk` to your Android device (Android 7.0+ / SDK 24+).
2. Tap the downloaded file to install. Allow *"Install unknown apps"* if prompted.
3. Open **Zaldo** to experience finance redefined.
4. Existing users can also check for over-the-air updates from **Profile > Check for Updates**.

---

## 🚀 Key Features

### 1. 🔔 Zero-Touch Financial Detection Engine
- **Notification & SMS Automation**: Runs a dedicated on-device listener (`FinancialNotificationListener`) parsing transaction notifications and bank SMS in real-time.
- **Universal Indian UPI Support**: Covers Google Pay, PhonePe, Paytm, Navi UPI (`com.naviapp`), CRED, BHIM, Amazon Pay, Super.money, Slice, Tata Neu, and all major Indian banks (SBI, HDFC, ICICI, Axis, Kotak, PNB, BOB, etc.).
- **Deterministic Semantic Parsing**: Distinguishes debit vs. credit (e.g., *"Money Received"*, *"Cashback"*, *"Salary Credited"*, *"Refund"*) without sign inversion.
- **Cryptographic Deduplication**: Generates deterministic SHA-256 signatures for transaction events to eliminate duplicate notifications and cross-app replay.

### 2. 📷 Deterministic Financial OCR Engine
- **Multi-Pass Structural & Geometric Parsing**: Processes payment screenshots and paper receipts with 100% precision across Navi, BHIM, CRED, PhonePe, Paytm, and Google Pay.
- **Noise Pre-Scrubbing**: Automatically isolates VPAs, masked account numbers, and phone numbers before amount calculation.
- **Hero Height Dominance**: Ranks candidate figures by spatial bounding-box font height to accurately identify the hero amount even on complex multi-offer screens.

### 3. 👥 Referral & Network Tracking System
- **Instant Invite Flow**: Frictionless invite popup with real-time dynamic code generation.
- **Live Firestore Validation**: Verifies referral codes on the fly during registration, confirming valid inviter identities before submission.
- **Atomic Attribution & Badges**: Automatic attribution logging and live count display (*"X Joined"*).
- **One-Tap Sharing**: Instant deep-linked APK sharing via WhatsApp, Telegram, and standard Android system shares.

### 4. 🎙️ Voice AI Transaction Logger
- **Continuous Speech Recognition**: Real-time transcript preview during live speech input.
- **Natural Language Understanding**: Converts casual spoken sentences (e.g. *"Paid 450 rupees for lunch at Chai Point via Navi UPI"*) into categorized transaction drafts with automatic amount, merchant, and method extraction.

### 5. 🔒 Biometric Security & Autopay Vault
- **Biometric App Lock**: Supports Fingerprint, Face ID, and Device Credential fallback with background inactivity auto-locking.
- **Encrypted Local Room DB**: High-performance local SQLite database via AndroidX Room with foreign key cascade integrity.
- **Autopay & Mandate Detector**: Automatically parses upcoming subscription dues, SIPs, and recurring mandates from notification streams.

### 6. 📄 Professional Statement Export Engine
- **Bank-Grade PDF Generation**: Renders clean, branded PDF statements complete with monthly breakdowns, inflow/outflow metrics, and transaction ledgers.

---

## 🛠️ Tech Stack & Architecture

```
app/
 ├── data/                    # Room Database, DAOs, Repositories, Entities
 ├── engine/                  # Intent Classifier, TransactionParser, SpamFilter, Deduplication
 ├── notifications/           # Notification Listener Service, ZaldoNotificationManager
 ├── ocr/                     # ReceiptOcrParser, SmartDocumentScanner (ML Kit)
 ├── ui/                      # Jetpack Compose UI (Theme, Screens, Components)
 │    ├── auth/               # Login, Register, AppLockGatekeeper
 │    ├── components/         # Manual Entry, Log Hub, Voice Modal, Referral Popup
 │    └── ...                 # Activity, Profile, Analytics, Wishlist
 └── util/                    # ShareUtils, Audio, Formatters
```

| Component | Technology |
|---|---|
| **Language** | Kotlin 2.2 |
| **UI Framework** | Jetpack Compose + Material 3 |
| **Architecture** | Unidirectional Data Flow (UDF) + MVVM |
| **Local Database** | AndroidX Room (with KSP code generation) |
| **Concurrency** | Kotlin Coroutines & Reactive `StateFlow` |
| **Preferences** | AndroidX Jetpack DataStore Preferences |
| **Vision & ML** | Google ML Kit Text Recognition |
| **Cloud Backend** | Firebase Authentication, Google Identity, Cloud Firestore |
| **PDF Rendering** | Android Native `PdfDocument` Canvas |

---

## 🔒 Security & Privacy Architecture

- **100% On-Device Parsing**: Financial SMS and notification texts are analyzed exclusively inside memory on your device. OTPs and personal messages are discarded instantly.
- **Zero Raw Credential Storage**: No net banking passwords, UPI PINs, or card CVVs are ever requested or stored.
- **Granular Security Rules**: Cloud Firestore security rules enforce strict authentication boundaries, ensuring users can only read and write their own data.

---

## ⚙️ Building from Source

### Prerequisites
- Android Studio Ladybug / Meerkat or newer
- JDK 17 or JDK 21
- Android SDK 36 (compileSdk & targetSdk)

```bash
# 1. Clone repository
git clone https://github.com/anwar0085/zaldo.git
cd zaldo

# 2. Run unit tests
./gradlew testDebugUnitTest

# 3. Build Debug APK
./gradlew assembleDebug
# Generated at: app/build/outputs/apk/debug/app-debug.apk

# 4. Build Release APK
./gradlew assembleRelease
# Generated at: app/build/outputs/apk/release/app-release.apk
```

---

## 📄 License & Attribution

Designed and engineered with pride for **ZALDO**.  
*Powered by Ninetech. All rights reserved.*
