# 🏢 Apartment Management System

A full-stack web application for managing a 140-room apartment building — built to replace a manual notebook + Excel workflow with an AI-powered, automated solution.

**Live Demo:** [nanaliseh.github.io/apartment-demo](https://nanaliseh.github.io/apartment-demo)

---

## 📸 Screenshots

> Dashboard · Room Grid Map · AI Meter Reading · Billing Statement · Payment Slip Verification

---

## ✨ Features

### 📷 AI-Powered Meter Reading
- Upload batch photos of water/electricity meters
- Claude AI automatically reads the meter number and room number sticker from each photo
- Auto-fills readings into the correct room — no manual entry needed

### 🧾 Automated Billing
- Calculates water, electricity, parking, and rent fees per room automatically
- Supports per-room parking configuration (motorbike / car / both)
- One-click print all 140 bills at once — one page per room

### 🧾 Payment Slip Verification
- Upload tenant payment slip photos
- AI reads amount, date, bank, and recipient name
- Cross-checks against expected amount and flags suspicious/fake slips
- Verdict: ✅ Genuine / ⚠️ Suspicious / 🚨 Likely Fake

### 💰 Payment Tracking
- Visual room grid — color-coded by payment status
- Track paid/unpaid per room at a glance
- Monthly revenue summary

### 📬 Mail Tracking
- Log incoming packages and letters per room
- Auto-generate LINE notification messages
- Overdue reminders after configurable number of days
- Track: Arrived → Notified → Collected

### 📅 Monthly History
- Archive each month's data before starting the next
- Browse last 6 months of billing history
- Export any month to Excel (.xlsx)
- Previous meter readings auto-carry forward each month

### 🗺️ Dashboard
- Real-time stats: occupancy, payments, revenue
- Floor-by-floor summary with occupancy progress bars
- Interactive room map — 140 rooms color-coded by status

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 18, Vite |
| AI | Anthropic Claude API (claude-sonnet-4-6) |
| Backend/Proxy | Netlify Functions (serverless) |
| Export | SheetJS (Excel generation) |
| Hosting | GitHub Pages / Netlify |
| Storage | Browser localStorage |

---

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/NanaliseH/apartment-demo.git
cd apartment-demo

# Install dependencies
npm install

# Run locally
npm run dev

# Build for production
npm run build
```

### Environment Variables (for Netlify deployment)
```
ANTHROPIC_API_KEY=your_api_key_here
```

---

## 📁 Project Structure

```
apartment-demo/
├── src/
│   ├── App.jsx          # Main application (all components)
│   └── main.jsx         # Entry point
├── netlify/
│   └── functions/
│       └── ai-proxy.js  # Serverless proxy for Anthropic API
├── index.html
├── vite.config.js
└── netlify.toml
```

---

## 💡 Problem Solved

**Before:** Property manager recorded 140 meter readings by hand in a notebook, calculated bills manually, typed into Excel, and printed each bill one by one every month — taking an entire day.

**After:** Upload meter photos → AI reads everything → bills calculate automatically → print all 140 in one click. Monthly billing now takes under an hour.

---

## 📊 Real-World Scale

- **140 rooms** across 8 floors (Building 2, Floors 2–9)
- **3 utility types:** water, electricity, parking
- **~140 meter photos** processed by AI each month
- **Monthly Excel exports** for record keeping

---

## 🔮 Roadmap

- [ ] LINE OA integration — auto-send bills to tenants via LINE
- [ ] Webhook for automatic payment slip processing
- [ ] Multi-building support
- [ ] Tenant portal (self-service payment status)

---

## 👩‍💻 Author

**Nanalise Howe**
- Portfolio: [nanaliseh.github.io/portfolio-website](https://nanaliseh.github.io/portfolio-website)
- GitHub: [@NanaliseH](https://github.com/NanaliseH)

---

*Built as a real production tool for Sirisuk Mansion, Clarksville TN / Thailand*
