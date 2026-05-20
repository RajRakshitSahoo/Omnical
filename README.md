# ⚡ OmniCalc Pro

### Ultimate All-in-One Calculator & Converter Suite

A **production-grade, single-file web application** featuring 15 calculators, 19 converters, a graphing engine, futuristic cyberpunk UI with glassmorphism, neon glows, and smooth animations — all with zero dependencies.

---

## 🚀 Quick Start

Simply open `omnicalc-pro.html` in any modern browser. No installation, no build step, no server required.

```bash
# Option 1: Double-click the file
open omnicalc-pro.html

# Option 2: Serve locally
npx serve .
# or
python3 -m http.server 8080
```

---

## ✨ Features At a Glance

### 🧮 15 Calculator Modes

| Calculator | Features |
|---|---|
| **Standard** | Basic ops, memory functions (MC/MR/M+/M−), keyboard support, copy result |
| **Scientific** | sin/cos/tan, log/ln, factorial, powers, roots, π/e constants, DEG/RAD toggle, SHIFT mode |
| **Graphing** | Real-time canvas rendering, multiple equations, zoom/pan, color-coded curves |
| **Programmer** | HEX/DEC/OCT/BIN, bitwise ops (AND/OR/XOR/NOT), shift ops, interactive 32-bit display |
| **Date & Age** | Difference in days/weeks/months/years, business days, age calculator, leap year checker |
| **BMI** | Metric & imperial, categories with color-coded results |
| **GPA/CGPA** | Dynamic subjects, grade points, credit-weighted GPA |
| **EMI Loan** | Monthly EMI, total amount, interest breakdown with visual bar |
| **SIP Investment** | Maturity value, invested amount, estimated returns |
| **Percentage** | X% of Y, % change, reverse percentage, X is what % of Y |
| **Equation Solver** | Linear (ax+b=0) and Quadratic (ax²+bx+c=0) with step output |
| **Matrix** | Add, subtract, multiply, determinant, inverse, transpose — 2×2 to 4×4 |
| **Statistics** | Mean, median, mode, variance, standard deviation, min/max, sum |
| **Tax & Discount** | GST/VAT presets (5/12/18/28%), custom rates, discount stacking |
| **Unit Price** | Compare multiple products, price per unit, best value indicator |

---

### 🔄 19 Converter Modes

| Converter | Units |
|---|---|
| **Currency** | 23 currencies: USD, EUR, GBP, JPY, INR, CNY, AUD, CAD, CHF, KRW, SGD, HKD, BRL, MXN, AED, SAR, ZAR, NZD, SEK, NOK, THB, MYR, IDR |
| **Length** | m, km, cm, mm, mi, yd, ft, in, nmi, nm |
| **Weight & Mass** | kg, g, mg, lb, oz, t, st |
| **Temperature** | °C, °F, K, °R — with reference table |
| **Area** | m², km², cm², ft², in², ac, ha, mi² |
| **Volume** | L, mL, m³, gal, qt, pt, cup, fl oz |
| **Speed** | m/s, km/h, mph, knot, ft/s, Mach |
| **Time** | ns, μs, ms, s, min, h, d, wk, mo, yr |
| **Energy** | J, kJ, cal, kcal, Wh, kWh, BTU |
| **Power** | W, kW, MW, hp, BTU/hr |
| **Data Storage** | bit, B, KB, MB, GB, TB, Mb, Gb |
| **Pressure** | Pa, kPa, bar, atm, PSI, mmHg |
| **Angle** | deg, rad, grad, turn, arcmin, arcsec |
| **Color** | HEX ↔ RGB ↔ HSL, color picker, swatches, copy buttons |
| **Number Base** | Binary, Octal, Decimal, Hexadecimal |
| **Roman Numerals** | Roman ↔ Decimal (1–3999), quick reference table |
| **Internet Speed** | bps/Kbps/Mbps/Gbps/MBps — download time estimator |
| **Screen Resolution** | Pixels ↔ Inches, aspect ratio, PPI calculator, presets |
| **Time Zone** | 12 major world time zones, live UTC reference |

---

## 🎨 UI & Design

- **Cyberpunk dark theme** — deep navy/black background with grid overlay
- **Glassmorphism cards** — backdrop blur, translucent panels
- **Neon glow effects** — purple/blue accent colors with box shadows
- **Animated transitions** — smooth fade + slide between modes
- **Interactive bits** — clickable 32-bit display in Programmer mode
- **Responsive layout** — sidebar collapses on small screens
- **Custom scrollbars** — styled to match the theme
- **Google Fonts** — Orbitron (headings), Exo 2 (body), JetBrains Mono (numbers)

---

## 📋 App Features

### History System
- Every calculation is automatically saved
- View full history from the clock icon in the top bar
- Copy any result to clipboard
- Delete individual entries or clear all
- Badge shows unread count

### Export
- Click the **📥 download** button to export history as a `.txt` file
- Compatible with any text editor or spreadsheet

### Keyboard Shortcuts (Standard Calculator)
| Key | Action |
|---|---|
| `0–9` | Number input |
| `+` `-` `*` `/` | Operators |
| `Enter` | Calculate |
| `Backspace` | Delete last digit |
| `Escape` | Clear |
| `.` | Decimal point |
| `%` | Percentage |

### Sidebar
- **Search bar** — filter all 34 tools instantly
- **Collapse button** — icon-only compact mode
- **Active indicator** — highlighted current tool with color accent
- Persistent state across reloads (localStorage)

### Persistent State
All of the following survive page reloads:
- Active calculator/converter mode
- Sidebar collapsed/expanded state
- Full calculation history (up to 200 entries)

---

## 🌐 Browser Compatibility

| Browser | Support |
|---|---|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Mobile browsers | ✅ Responsive |

---

## 📁 Project Structure

```
omnicalc-pro/
├── omnicalc-pro.html    ← Complete application (single file)
└── README.md            ← This file
```

The entire application is contained in a single HTML file (~1,500 lines) with:
- Vanilla JavaScript (ES2020+)
- Inline CSS with CSS custom properties
- No external JavaScript dependencies
- Google Fonts loaded from CDN (internet required for fonts only)
- All math computed in-browser

---

## 🔧 Customization

### Adding a Currency Rate
Find the `RATES` object in the `<script>` section:
```js
const RATES = { USD: 1, EUR: 0.92, ... };
```
Add your currency: `XYZ: 1.23`
Also add a flag emoji to `FLAGS`: `XYZ: '🏳️'`

### Adding a Unit Converter
Find `UNIT_DEFS` and add a new entry:
```js
myunit: {
  units: [{id:'a', l:'Unit A'}, {id:'b', l:'Unit B'}],
  base:  {a: 1, b: 2.5},   // values relative to a base unit
  title: 'My Unit',
  color: '#00e5ff'
}
```
Then add a renderer mapping in `RENDERERS`:
```js
myunit: () => renderGenericConverter('myunit')
```
And add a nav entry in `MODES`.

### Changing Theme Colors
Key CSS variables / hex values to change:
- Purple accent: `#b429f9`
- Blue accent: `#2979ff`
- Cyan accent: `#00e5ff`
- Green accent: `#00e676`
- Background: `#020409`
- Card background: `rgba(10,22,40,0.7)`

---

## 📐 Technical Details

### Graphing Engine
- Pure HTML5 Canvas (no Plotly/Chart.js)
- Evaluates equations using `Function()` constructor
- Adaptive Y-axis scaling
- Grid lines with auto-step size
- Glow effects via `shadowBlur`
- Supports all Math functions: `Math.sin`, `Math.cos`, `Math.sqrt`, etc.

### Equation format for graphing:
```
Math.sin(x)
Math.pow(x, 2)
Math.exp(-x * x / 2)
x**3 - 3*x
Math.log(x)
```

### Matrix Operations
- Gaussian elimination for inverse
- Cofactor expansion for determinant
- Supports 2×2, 3×3, 4×4 matrices

### Statistics Engine
- Population variance (σ²) and standard deviation (σ)
- Handles multi-modal datasets
- Input: comma or whitespace separated

---

## ⚙️ For Developers: React Version

A full React + Vite project scaffold is included in the repository for teams who want to extend this into a full application:

```bash
npm install
npm run dev
```

**Stack:** React 18, Vite 5, Tailwind CSS 3, Framer Motion 11, Zustand 4, mathjs 12, Plotly.js, react-hot-toast, jsPDF

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

## 🙌 Credits

Built with ❤️ using:
- [Google Fonts](https://fonts.google.com/) — Orbitron, Exo 2, JetBrains Mono
- Vanilla JS + HTML5 Canvas
- Pure CSS glassmorphism & neon effects

---

*OmniCalc Pro — Where every calculation meets its match.*
