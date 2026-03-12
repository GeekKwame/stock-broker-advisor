# 📈 Dodgy Dave's Stock Predictions

A fun, tongue-in-cheek stock prediction web app that fetches real market data from the [Polygon.io](https://polygon.io/) API and generates AI-powered "predictions" using OpenAI. Built with vanilla HTML, CSS, and JavaScript, bundled with [Vite](https://vitejs.dev/).

> **Disclaimer:** This is **not** real financial advice — "Always correct 15% of the time!" 😜

![Dodgy Dave's Stock Predictions](images/logo-dave-text.png)

---

## ✨ Features

- **Stock Ticker Input** — Add up to 3 stock tickers (e.g. `MSFT`, `TSLA`, `AAPL`)
- **Real Market Data** — Fetches recent daily aggregates from the Polygon.io REST API
- **AI-Generated Reports** — Sends stock data to OpenAI for a humorous "analysis" *(integration placeholder)*
- **Loading States** — Visual feedback with an animated loader while data is fetched
- **Responsive UI** — Clean layout with Google Fonts (Poppins, Comic Neue) and normalize.css

---

## 🗂️ Project Structure

```
stock-broker-advisor/
├── images/
│   ├── add.svg              # Add-ticker button icon
│   ├── loader.svg            # Loading spinner
│   └── logo-dave-text.png    # Header logo
├── open-ai-dependency/       # Scaffold for OpenAI integration
│   ├── index.html
│   ├── index.css
│   └── index.js
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
- An [OpenAI](https://platform.openai.com/) API key

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
   POLYGON_API_KEY=your_polygon_api_key_here
   OPENAI_API_KEY=your_openai_api_key_here
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
3. **AI Report** — The fetched data is passed to an AI report generator (OpenAI integration placeholder in `fetchReport()`).
4. **View Results** — The report is rendered in the output panel.

### Key Files

| File | Role |
| --- | --- |
| `index.js` | Handles form input, API calls to Polygon.io, and report rendering |
| `utils/dates.js` | Computes `startDate` (3 days ago) and `endDate` (yesterday) in `YYYY-MM-DD` format |
| `index.html` | Semantic HTML structure with action, loading, and output panels |
| `index.css` | Styling with Poppins + Comic Neue fonts, responsive panels |

---

## 📦 Dependencies

| Package | Purpose |
| ------- | ------- |
| **openai** | OpenAI SDK for generating AI reports |
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
