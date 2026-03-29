<div align="center">

# ⚡ NetSec Academy

### Networking for Cybersecurity

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![No Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)
![Responsive](https://img.shields.io/badge/responsive-mobile--first-blue)

**A free, single-file web app teaching computer networking for cybersecurity students.**  
16 structured modules · Interactive diagrams · Interview prep · Zero dependencies

[🚀 Live Demo](#) · [📖 Modules](#-modules) · [🤝 Contributing](#-contributing) · [📄 License](#-license)

</div>

---

## 📋 Table of Contents

- [About](#-about)
- [Features](#-features)
- [Modules](#-modules)
- [Getting Started](#-getting-started)
- [Deployment](#-deployment)
- [Responsive Design](#-responsive-design)
- [File Structure](#-file-structure)
- [Tech Stack](#-tech-stack)
- [Browser Support](#-browser-support)
- [Contributing](#-contributing)
- [License](#-license)
- [Credits](#-credits)

---

## 🎯 About

**NetSec Academy** is a self-contained HTML learning platform covering networking fundamentals from the ground up — specifically tailored for cybersecurity. It covers everything from IP addressing and the OSI model to real-world attack techniques like ARP spoofing and DDoS.

Built for:
- 🔰 Cybersecurity beginners building their networking foundation
- 🎓 Students studying for **CompTIA Security+**, **CEH**, or **OSCP**
- 💼 Anyone preparing for **SOC analyst** or **penetration tester** interviews

> Everything ships in a **single `.html` file** — no server, no npm, no build step.

---

## ✨ Features

| Feature | Description |
|---|---|
| 📚 **16 Modules** | Structured curriculum from networking basics to attack techniques |
| 🎨 **Interactive Diagrams** | Canvas-based animated visualizations (TCP handshake, DDoS, DNS flow, and more) |
| 🃏 **Interview Prep Cards** | Click-to-reveal Q&A cards with real SOC/networking interview questions |
| 🎯 **Attack Reference Grid** | Quick-reference cards covering 6 major network attack types |
| ▶️ **Curated Videos** | Recommended YouTube videos per module from David Bombal, NetworkChuck, and more |
| 📱 **Fully Responsive** | Mobile-first design with slide-in drawer navigation for phones and tablets |
| 🌐 **Zero Dependencies** | No frameworks, no CDN runtimes — works completely offline |

---

## 📖 Modules

<details>
<summary><strong>Click to expand all 16 modules</strong></summary>

| # | Module | Key Topics |
|---|---|---|
| 01 | Introduction to Networking | Networks, LAN/WAN, topologies, devices |
| 02 | How the Internet Works | Packets, ISPs, routing, BGP basics |
| 03 | IP Addressing | IPv4, IPv6, subnetting, CIDR notation |
| 04 | Ports & Protocols | Well-known ports, TCP/UDP, protocol overview |
| 05 | OSI Model | All 7 layers with cybersecurity relevance |
| 06 | TCP/IP Model | The 4-layer model, comparison with OSI |
| 07 | TCP vs UDP Deep Dive | 3-way handshake, reliability, use cases |
| 08 | DNS Deep Dive | Resolution flow, record types, DNS attacks |
| 09 | Network Communication Flow | End-to-end data path, ARP, MAC addresses |
| 10 | Packet Fundamentals | Headers, encapsulation, Wireshark basics |
| 11 | Traffic Analysis | Sniffing, anomaly detection, Wireshark filters |
| 12 | Network Architecture | DMZ, VLANs, segmentation, zero trust |
| 13 | NAT & Routing | NAT types, routing tables, BGP basics |
| 14 | Firewalls & Network Security | Stateful/stateless, WAF, IDS/IPS |
| 15 | Network Monitoring & Logging | SIEM, NetFlow, syslog, log analysis |
| 16 | Network Attacks Overview | Port scanning, MITM, ARP spoofing, DDoS, DNS poisoning |

</details>

---

## 🚀 Getting Started

### Option 1 — Open directly (quickest)

Just download and double-click the HTML file. Works in any modern browser with zero setup.

### Option 2 — Serve locally (recommended)

Running over HTTP ensures canvas diagrams and animations load correctly:

```bash
# Python 3
python -m http.server 8080

# Node.js
npx serve .

# PHP
php -S localhost:8080
```

Then visit: `http://localhost:8080/netsec-academy-responsive.html`

### Option 3 — Clone and run

```bash
git clone https://github.com/YOUR-USERNAME/netsec-academy.git
cd netsec-academy
python -m http.server 8080
```

---

## 🌍 Deployment

### GitHub Pages *(recommended — free)*

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)` folder
4. Your site will be live at `https://YOUR-USERNAME.github.io/netsec-academy/`

> **Tip:** Rename the HTML file to `index.html` so it serves automatically at the root URL.

### Other platforms

| Platform | Steps |
|---|---|
| **Netlify** | Drag-and-drop the HTML file at [app.netlify.com](https://app.netlify.com) |
| **Vercel** | `npx vercel` in the project folder |
| **Cloudflare Pages** | Connect repo → build command: *(none)*, output directory: `/` |

---

## 📱 Responsive Design

Fully optimized across all screen sizes:

| Breakpoint | Behavior |
|---|---|
| **Desktop** `> 960px` | Fixed sidebar on left, scrollable content on right |
| **Tablet** `≤ 960px` | Sidebar hidden; ☰ hamburger opens a slide-in drawer |
| **Large Phone** `≤ 700px` | 2-column grids, stacked buttons, compact stats bar |
| **Small Phone** `≤ 420px` | Single-column layout, optimized font sizes |
| **Landscape Phone** | Reduced header height, drawer fits short viewports |

**Mobile navigation:**
- Tap **☰** (top-right) to open the module drawer
- Tap any module → navigates and auto-closes the drawer
- Tap the **✕** button, the dark overlay, or press `Esc` to close
- All interactive elements have enlarged touch targets on touch screens

---

## 📁 File Structure

```
netsec-academy/
├── netsec-academy-responsive.html   ← Entire app (single file)
├── README.md                        ← This file
└── LICENSE                          ← MIT License
```

Inside the HTML file:

```
netsec-academy-responsive.html
├── <head>
│   ├── Google Fonts (JetBrains Mono, Plus Jakarta Sans, Outfit)
│   ├── CSS custom properties & design tokens
│   ├── Component styles (cards, tables, diagrams, code blocks)
│   ├── Responsive breakpoints (960px / 700px / 420px / landscape)
│   └── Canvas utility library (_U object)
└── <body>
    ├── #header           — Fixed top bar: logo + nav + hamburger
    ├── .sidebar-overlay  — Mobile backdrop (tap to close)
    ├── nav.sidebar       — Slide-in module drawer
    └── main.content
        ├── #page-home           — Hero, stats, learning roadmap
        └── #page-networking
            └── #mod-m1 … #mod-m16  — 16 modules with text,
                                       diagrams, code blocks,
                                       interview cards, videos
```

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Markup | Semantic HTML5 |
| Styling | Pure CSS3 with custom properties |
| Scripting | Vanilla JavaScript (ES6+) |
| Diagrams | HTML5 Canvas API + custom `_U` utility library |
| Fonts | Google Fonts — JetBrains Mono, Plus Jakarta Sans, Outfit |
| Icons | Unicode emoji — no icon library needed |

**No npm. No webpack. No React. No build step.** Just open and learn.

---

## 🌐 Browser Support

| Browser | Minimum Version |
|---|---|
| Chrome / Edge | 88+ |
| Firefox | 85+ |
| Safari | 14+ |
| Samsung Internet | 14+ |
| iOS Safari | 14.4+ |

Requires: CSS Grid, CSS Custom Properties, Canvas API, `IntersectionObserver`, `backdrop-filter`.

---

## 🤝 Contributing

Contributions are welcome! Here's how:

```bash
# 1. Fork the repo on GitHub

# 2. Clone your fork
git clone https://github.com/YOUR-USERNAME/netsec-academy.git

# 3. Create a feature branch
git checkout -b feature/add-vpn-module

# 4. Make your changes, then commit
git add .
git commit -m "feat: add module 17 - VPN and tunneling protocols"

# 5. Push and open a Pull Request
git push origin feature/add-vpn-module
```

### Ideas for contributions

- 🆕 New modules — VPNs, wireless security, cloud networking, IPv6 deep dive
- 🐛 Bug fixes or layout improvements
- 🌍 Translations / localization
- 📝 Content corrections or clarifications
- 🎨 New interactive canvas diagrams

> Please keep the **single-file constraint** — all changes should stay within the one HTML file.

---

## 📄 License

```
MIT License

Copyright (c) 2025 NetSec Academy

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Credits

- **Video content** — [David Bombal](https://www.youtube.com/@davidbombal), [NetworkChuck](https://www.youtube.com/@NetworkChuck), [The Cyber Mentor](https://www.youtube.com/@TCMSecurityAcademy) on YouTube
- **Fonts** — [Google Fonts](https://fonts.google.com) — JetBrains Mono, Plus Jakarta Sans, Outfit
- **Inspired by** — The open cybersecurity education community

---

<div align="center">

Made with ❤️ for the cybersecurity community

**⭐ Star this repo if it helped you learn!**

</div>
