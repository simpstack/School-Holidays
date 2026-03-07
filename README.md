# 🗓 School Holidays UK

A clean, Apple-inspired web app to look up school term dates and holidays for any school or local authority in the UK — powered by Claude AI.

![School Holidays UK](https://img.shields.io/badge/status-live-brightgreen) ![License](https://img.shields.io/badge/license-MIT-blue)

## ✨ Features

- 🔍 Search any UK school or local authority
- 📅 Supports academic years 2023–24 through 2026–27
- 🎨 Clean Apple-inspired design
- ⚡ Quick-search pills for common councils (Wokingham, Reading, Hampshire…)
- 📋 Results grouped by term, collapsible
- 📱 Fully responsive
- 🚀 Zero dependencies — single HTML file

## 🚀 Deploy to GitHub Pages

1. **Fork or clone** this repo
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)` folder
4. Visit `https://yourusername.github.io/school-holidays`

That's it — no build step required.

## 🔑 API Key

This app calls the [Anthropic Claude API](https://www.anthropic.com) directly from the browser.

- **On Claude.ai** — the API key is handled automatically (no setup needed)
- **On GitHub Pages / self-hosted** — you need to add your API key

To add your key for self-hosting, open `index.html` and find the fetch call, then add your key to the headers:

```js
headers: {
  'Content-Type': 'application/json',
  'anthropic-version': '2023-06-01',
  'x-api-key': 'YOUR_API_KEY_HERE',        // ← add this line
  'anthropic-dangerous-direct-browser-access': 'true'
}
```

> ⚠️ **Never commit your API key to a public repo.** For production use, route API calls through a backend proxy.

## 📁 File Structure

```
school-holidays/
└── index.html     # Entire app — HTML, CSS, JS in one file
└── README.md
```

## ⚠️ Disclaimer

Holiday dates are AI-generated and may not reflect individual school or academy trust variations. Always verify with your school or [GOV.UK](https://www.gov.uk/school-term-holiday-dates).

## 📄 License

MIT — free to use, modify, and deploy.
