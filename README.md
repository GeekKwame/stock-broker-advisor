# 📈 Dodgy Dave's Stock Predictions

A fun, tongue-in-cheek stock prediction web app that fetches real market data from the [Polygon.io](https://polygon.io/) API and generates AI-powered reports and recommendations using Google Gemini. Built with vanilla HTML, CSS, and JavaScript, bundled with [Vite](https://vitejs.dev/).

> **Disclaimer:** This is **not** real financial advice — "Always correct 15% of the time!" 😜

![Dodgy Dave's Stock Predictions](images/logo-dave-text.png)

---

## ✨ Features

- **Stock Ticker Input** — Add up to 3 stock tickers (e.g. `MSFT`, `TSLA`, `AAPL`)
- **Real Market Data** — Fetches recent daily aggregates from the Polygon.io REST API
- **AI-Generated Reports** — Sends stock data to Google Gemini for a professional analysis and buy/sell recommendation
- **Loading States** — Visual feedback with an animated loader while data is fetched
- **Responsive UI** — Clean layout with Google Fonts (Poppins, Comic Neue) and normalize.css

---

## 🗂️ Project Structure

```text
stock-broker-advisor/
├── images/
│   ├── add.svg              # Add-ticker button icon
│   ├── loader.svg            # Loading spinner
│   └── logo-dave-text.png    # Header logo
├── utils/
│   └── dates.js              # Date helpers (start/end date for API calls)
├── index.html                # Main entry point
├── index.css                 # Styles
├── index.js                  # Core application logic
├── vite.config.js            # Vite configuration
├── package.json              # Dependencies & scripts
├── .env                      # Environment variables (not committed)
└── .gitignore
```

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v16+)
- A [Polygon.io](https://polygon.io/) API key (free tier available)
- A [Google Gemini](https://aistudio.google.com/apikey) API key

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/GeekKwame/stock-broker-advisor.git
   cd stock-broker-advisor
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Configure environment variables**

   Create a `.env` file in the project root (it's git-ignored by default):

   ```env
   VITE_POLYGON_API_KEY=your_polygon_api_key_here
   VITE_GEMINI_API_KEY=your_gemini_api_key_here
   ```

4. **Start the dev server**

   ```bash
   npm start
   ```

   The app will open at `http://localhost:5173` (default Vite port).

---

## 🛠️ Scripts

| Command           | Description                        |
| ----------------- | ---------------------------------- |
| `npm start`       | Start the Vite dev server          |
| `npm run dev`     | Alias for `npm start`              |
| `npm run build`   | Build for production               |
| `npm run preview` | Preview the production build       |

---

## 🔧 How It Works

1. **Enter tickers** — Type a stock ticker (≥ 3 characters) and click the ➕ button to add it. Up to 3 tickers are accepted.
2. **Generate Report** — Click *Generate Report* to fetch daily aggregate data from Polygon.io for the last 3 days.
3. **AI Report** — The fetched data is passed to the Google Gemini AI model (in `fetchReport()`) to generate an HTML-formatted analysis.
4. **View Results** — The report is rendered beautifully in the output panel.

### Key Files

| File | Role |
| --- | --- |
| `index.js` | Handles form input, API calls to Polygon.io, and report rendering |
| `utils/dates.js` | Computes `startDate` (3 days ago) and `endDate` (yesterday) in `YYYY-MM-DD` format |
| `index.html` | Semantic HTML structure with action, loading, and output panels |
| `index.css` | Styling with Poppins + Comic Neue fonts, flexbox & responsive panels |

---

## 📦 Dependencies

| Package | Purpose |
| ------- | ------- |
| **@google/generative-ai** | Google Gemini SDK for generating AI reports |
| **vite** *(dev)* | Fast build tool and dev server |

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is open source and available for personal and educational use.

---

> Built with ❤️ by [GeekKwame](https://github.com/GeekKwame)
