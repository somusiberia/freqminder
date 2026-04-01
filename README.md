# FreqFinder

**RF channel coordination tool for wireless microphones**

🎤 Подбор частот для радиомикрофонов • RF frequency finder for wireless mic systems

---

## Features

✨ **Frequency Management**
- Add/edit wireless microphone channels
- Real-time frequency validation
- Support for Sennheiser bands (A1, A, AS, G, GB, B, C, D, E, JB, K+, 1G8)

🔍 **Advanced Analysis**
- Intermodulation (IM) detection up to 15th order
- Guard band violation detection
- Frequency proximity warnings
- Multi-channel conflict analysis

🎯 **Smart Frequency Finder**
- Automatic scan for free frequencies in selected band
- Respects guard intervals and IM products
- One-click channel addition at suggested frequencies

📱 **PWA Support**
- Installable as standalone app on iOS/Android
- Offline-first with Service Worker
- Full-screen mode support
- Bilingual UI (English / Русский)

💾 **List Management**
- Save multiple frequency configurations
- Rename/delete saved lists
- Transmitter brand/model tracking (Sennheiser, Lectrosonics, Shure, Sony, etc.)

---

## Quick Start

### Option 1: Web (Recommended for iPhone)
1. Open in Safari: [https://somusiberia.github.io/freqminder/](https://somusiberia.github.io/freqminder/)
2. Tap **Share** → **Add to Home Screen**
3. Use like a native app

### Option 2: Single-File HTML
1. Download `freqfinder-standalone.html`
2. On iPhone: Open in **Files** app from Safari
3. Tap and select "Open in Safari"

### Option 3: Self-Hosted
1. Clone this repo
2. Serve over **HTTPS** (e.g., GitHub Pages, Vercel, Netlify)
3. Add to home screen in Safari for PWA experience

---

## Files

```
├── index.html              # Main HTML structure
├── script.js              # Core logic (frequency analysis, IM products)
├── styles.css             # iOS-inspired liquid glass design
├── manifest.webmanifest   # PWA configuration
├── icon.svg               # App icon
├── sw.js                  # Service Worker (offline support)
├── build-standalone.ps1   # Build script for single-file HTML
└── README.md              # This file
```

---

## Development

### Build Standalone HTML (Windows PowerShell)
```powershell
.uild-standalone.ps1
```
Creates:
- `freqfinder-standalone.html` (complete in one file)
- `FreqFinder-iPhone.html` (copy for mobile sharing)

---

## Frequency Analysis

### Intermodulation Detection
The app checks **odd-order IM products** up to configurable order (default: 7th):

**2nd-order pairs:**
- `f1 ± f2`

**3rd-order triples:**
- `f1 + f2 − f3`
- `2·f1 − f2`

Higher orders follow similar patterns.

### Guard Interval
Adjustable separation between frequencies (default: 0.2 MHz).
Prevents adjacent channel interference.

---

## Supported Transmitter Brands

- **Sennheiser**: XS Wireless, ew 100/300/500 G2-G4, SK series
- **Lectrosonics**: SMQV, SMV, SMWB, SMDWB, LT, LMb, HMa, HHa, IFB T4, DSQD
- **Sound Devices**: A10-TX
- **Shure**: GLX-D+, SLXD1, QLXD1, ULXD1, AD1, ADX1
- **Sony**: UWP-D, DWX
- **Audio-Technica**: 3000/4000/5000 Series, System 10 Pro
- **Wisycom**: MTP40, MTP41, MTP60, MTH400
- **Zaxcom**: ZMT3, ZMT4, TRXLA3
- **RØDE**: Wireless GO II, Wireless PRO
- **Deity**: Theos, BP-TRX
- **MiPro**: ACT series, MI-909
- **CAD Audio**: WX1610

---

## Storage

All data saved locally in browser:
- `freqfinder-channels-v2` → Current channel list
- `freqfinder-saved-lists-v1` → Saved frequency configurations
- `freqfinder-workspace-v1` → Current session state
- `freqfinder-lang` → UI language preference
- `freqfinder-im-max-order` → IM analysis order setting

No server required. No tracking. Privacy-first.

---

## Browser Support

✅ **iOS Safari** (14+) — Recommended
✅ **Chrome/Edge** (Android, Desktop)
✅ **Firefox** (Desktop)
⚠️ **Safari macOS** — Partial backdrop-filter support

---

## Design

**Color Palette:** HC Sibir (Deep blues + ice frost)
- Primary: `#4a9fe8` (bright blue)
- Accent: `#1e5a8e` (deep blue)
- Background: `#e3f0fa` (mist)

**Typography:** System fonts (SF Pro, Segoe UI, Roboto)

---

## License

MIT (or specify your license)

---

## Contributing

Pull requests welcome! For major changes:
1. Open an issue first
2. Describe your improvement
3. Test on iOS and desktop

---

## Contact

For questions/suggestions: [your-email-or-link]

**Made with ❄️ for broadcast professionals**