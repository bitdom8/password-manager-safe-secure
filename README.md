# 🔐 Pass Mega Secure Notes

> **Military-grade encrypted note-taking with zero-knowledge architecture**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Security](https://img.shields.io/badge/security-military--grade-green.svg)](https://github.com/yourusername/secure-notes)
[![Privacy](https://img.shields.io/badge/privacy-zero--knowledge-brightgreen.svg)](https://github.com/yourusername/secure-notes)

## 🌟 What Makes This Special?

Your thoughts, ideas, and sensitive information deserve the highest level of protection. **Secure Notes** combines end-to-end encryption, biometric authentication, and multi-device sync to create the most secure note-taking experience available.

**Unlike traditional note apps**, every single note is encrypted on your device before it ever leaves. Not even we can read your notes. That's the power of zero-knowledge architecture.

## ✨ Features

### 🛡️ Bank-Level Security
- **XChaCha20-Poly1305 AEAD** - Military-grade authenticated encryption
- **Argon2id Key Derivation** - Winner of the Password Hashing Competition, GPU-resistant
- **Zero-Knowledge Architecture** - Your notes are encrypted before leaving your device
- **WebAuthn Biometrics** - Unlock with fingerprint or Face ID
- **DOMPurify XSS Protection** - Advanced sanitization prevents code injection
- **Replay Attack Prevention** - Nonce validation and timestamp verification

### 💎 Powerful Features
- 📱 **Multi-Device Sync** - Access notes on any device with encrypted cloud sync
- 📤 **Encrypted Export/Import** - Password-protected backups with conflict resolution
- 🔍 **Instant Search** - Real-time search across all notes, works offline
- 💾 **Offline-First** - All encryption happens locally, no internet required
- 🔒 **Auto-Lock** - Vault locks after 5 minutes of inactivity
- 📊 **Device Management** - Track and remove devices that accessed your vault
- 🚫 **No Tracking** - Zero analytics, no cookies, complete privacy

## 🆚 How We Compare

| Feature | Secure Notes | Google Keep | Evernote | Apple Notes |
|---------|-------------|-------------|----------|-------------|
| End-to-End Encryption | ✅ | ❌ | ❌ | ✅ |
| Zero-Knowledge | ✅ | ❌ | ❌ | ❌ |
| Biometric Unlock | ✅ | ❌ | ❌ | ✅ |
| Device Alerts | ✅ | ❌ | ❌ | ❌ |
| Open Source Crypto | ✅ | ❌ | ❌ | ❌ |
| Cross-Platform | ✅ | ✅ | ✅ | ❌ |
| Free Forever | ✅ | ✅ | ❌ | ✅ |

## 🔒 Security Deep Dive

### What We Store (Encrypted)
- ✅ Your encrypted notes (gibberish without your password)
- ✅ Device identifiers (for device management)
- ✅ Last sync timestamp (for conflict resolution)
- ✅ Encrypted salt (for key derivation)

### What We NEVER Store
- ❌ Your master password
- ❌ Your encryption keys
- ❌ Plain text notes
- ❌ Biometric data
- ❌ IP logs or analytics
- ❌ Personal information

### Real-World Protection

**Scenario: Server Gets Hacked**
- With Secure Notes: Attackers get encrypted blobs. Breaking it would take trillions of years.
- With other apps: Attackers instantly read all your notes.

**Scenario: Government Subpoena**
- With Secure Notes: We hand over encrypted blobs. Still unreadable without your password.
- With other apps: Government gets full access immediately.

## ⚙️ Technology Stack

- **libsodium-sumo** - Cryptographic library trusted by Signal and WhatsApp
- **Argon2id** - Memory-hard password hashing algorithm
- **XChaCha20-Poly1305** - Authenticated encryption with extended nonce
- **WebAuthn** - W3C standard for biometric authentication
- **IndexedDB** - Client-side encrypted storage
- **Alpine.js** - Lightweight reactive framework
- **Bun + SQLite** - High-performance backend with WAL mode
- **DOMPurify** - XSS sanitization library

## 🚀 Quick Start

### For Users

1. Visit the live app: [https://yourusername.github.io/secure-notes](https://yourusername.github.io/secure-notes)
2. Create your master password
3. Start taking encrypted notes!

### For Developers

```bash
# Clone the repository
git clone https://github.com/yourusername/secure-notes.git
cd secure-notes

# Install dependencies
bun install

# Start development server
bun dev

# Build for production
bun run build
```

## 📖 How It Works

1. **Master Password Creates Encryption Key** - Your password goes through Argon2id key derivation with a unique salt
2. **Local Encryption** - Each note is encrypted using XChaCha20-Poly1305 AEAD before storage
3. **Zero-Knowledge Sync** - Already-encrypted notes are sent to the cloud
4. **Multi-Device Access** - Enter your password on new devices to regenerate your encryption key
5. **Biometric Convenience** - WebAuthn stores your encrypted password locally for quick unlock

## 🔐 Security Guarantees

- **256-bit Encryption**: XChaCha20-Poly1305 provides authenticated encryption
- **Memory-Hard KDF**: Argon2id with 64MB RAM requirement makes brute-force attacks infeasible
- **Break Time**: With a strong 12-character password, breaking the encryption would take ~10²⁴ years
- **No Backdoors**: Open-source cryptography, verifiable by anyone
- **Client-Side Only**: All cryptographic operations happen in your browser

## 🌍 Privacy Philosophy

We believe privacy is a fundamental human right. That's why:

- ❌ No tracking or analytics
- ❌ No data selling
- ❌ No spam or marketing emails
- ❌ No AI training on your data
- ✅ Open source and transparent
- ✅ Zero-knowledge architecture
- ✅ You own your data

## 📋 Roadmap

- [ ] Mobile apps (iOS/Android)
- [ ] Browser extensions
- [ ] Rich text formatting
- [ ] File attachments (encrypted)
- [ ] Shared notes (end-to-end encrypted)
- [ ] Two-factor authentication
- [ ] Security audit by third-party firm

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Development

```bash
# Run tests
bun test

# Lint code
bun lint

# Format code
bun format
```

## 💰 Support Development

Secure Notes is completely free and open source. Your contributions help us keep it that way.

**USDT (TRC20) Wallet:**
```
TEehyL1WTGpU3psiFHWmBPBes6Xi1Az3we
```

## 📞 Contact & Support

- 📧 Telegram: [t.me/formegadmin](https://t.me/formegadmin)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Important Notes

- **Password Recovery**: Due to zero-knowledge encryption, we cannot recover your password. Keep it safe!
- **Backup Your Salt**: Export your encryption salt as a QR code or backup file
- **Strong Passwords**: Use a strong, unique password (12+ characters recommended)

## 🙏 Acknowledgments

- [libsodium](https://libsodium.gitbook.io/) for cryptographic primitives
- [Signal Protocol](https://signal.org/docs/) for security inspiration
- The open-source community for making privacy accessible

---

<div align="center">

**🔐 Your notes. Your privacy. Your control.**

[Launch App](https://yourusername.github.io/secure-notes) • [View Documentation](https://github.com/yourusername/secure-notes/wiki) • [Report Issue](https://github.com/yourusername/secure-notes/issues)

Made with ❤️ for privacy

</div>
