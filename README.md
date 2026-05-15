# Japan Car Import Advisory Platform 🇰🇪

AI-powered platform to help Kenyans calculate the real cost of importing cars from Japan and compare with local market prices.

## Features

- **Firecrawl Web Scraping**: Automated data collection from Japanese car auction sites and Kenyan dealerships
- **Real-time Price Comparison**: Compare Japan auction prices vs. local Kenyan market prices
- **Cost Calculator**: Calculate total import costs including:
  - Shipping fees
  - Customs duties
  - Insurance
  - VAT and other taxes
  - Transportation to destination
- **AI-Powered Insights**: Smart recommendations on best value imports based on market analysis
- **User-Friendly Dashboard**: Interactive interface for exploring car data and cost breakdowns

## Tech Stack

- **Frontend**: Streamlit / React
- **Backend**: Python / Node.js
- **Data Scraping**: Firecrawl API
- **Database**: PostgreSQL / MongoDB
- **AI/ML**: LangChain, OpenAI API
- **Deployment**: Kaggle / Cloud Platform

## Installation

### Prerequisites
- Python 3.8+
- API Keys: Firecrawl, OpenAI

### Setup

1. Clone the repository
```bash
git clone https://github.com/musiliandrew/Japan-Car-Import-Advisory-Platform-for-Kenyan-Buyers.git
cd Japan-Car-Import-Advisory-Platform-for-Kenyan-Buyers
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Create `.env` file with your API keys
```
FIRECRAWL_API_KEY=your_key_here
OPENAI_API_KEY=your_key_here
```

4. Run the application
```bash
streamlit run app.py
```

## Usage

1. **Search for Cars**: Enter vehicle make/model and year
2. **View Japan Prices**: See current auction prices from Japanese sources
3. **Calculate Total Cost**: Get breakdown of all import expenses
4. **Compare Prices**: See how import cost compares to local market price
5. **Get Recommendations**: AI insights on best value options

## Project Structure

```
├── src/
│   ├── scrapers/          # Web scraping modules
│   ├── calculators/       # Cost calculation logic
│   ├── ai/                # AI/ML models
│   └── utils/             # Helper functions
├── data/                  # Data storage
├── app.py                 # Main Streamlit app
├── requirements.txt       # Dependencies
└── README.md             # This file
```

## API Integration

### Firecrawl
Used for intelligent web scraping of:
- Japanese car auction sites
- Kenyan dealership listings
- Exchange rate data

### OpenAI
Powers the recommendation engine to:
- Analyze market trends
- Provide buying insights
- Generate cost optimization suggestions

## Data Sources

- Japanese car auctions (Goo, Autotrader Japan, etc.)
- Kenya vehicle marketplaces (Cars45, Autochek, etc.)
- Current exchange rates
- Shipping quotes from logistics providers

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer

This platform is for informational purposes only. Always conduct thorough research and consult with automotive experts before importing vehicles. Import regulations and taxes may vary; verify current rates with relevant Kenyan authorities.

## Contact & Support

For questions or feedback, reach out via:
- GitHub Issues
- Email: [your-email@example.com]
- Twitter: [@your-handle]

---

**Made with ❤️ for Kenyan car enthusiasts**
