# Gold Prices vs US 10-Year Treasury Yield Analysis

## 📊 Project Overview

An exploratory data analysis investigating the relationship between US 10-Year Treasury yields and gold prices over a 20-year period (2004-2025). This project tests the classical economic theory that rising bond yields reduce demand for non-yielding assets like gold.

**Key Question:** Does rising Treasury yield really cause gold prices to drop?

---

## 🎯 Objectives

- Analyze the correlation between US 10Y Treasury yields and gold prices
- Examine how this relationship changes over different economic periods
- Test whether the "opportunity cost" theory holds in real market data
- Identify periods where the relationship breaks down

---

## 📁 Project Structure

```
├── gold_us10y_analysis.ipynb          # Main Jupyter notebook with full analysis
├── gold_vs_us10y_data.csv             # Cleaned dataset (generated)
├── README.md                          # Project documentation
├── requirements.txt                   # Python dependencies
└── visualizations/                    # Generated plots (optional folder)
    ├── gold_vs_yield_timeseries.png
    ├── gold_vs_yield_scatter.png
    ├── rolling_correlation.png
    ├── period_comparison.png
    └── final_summary.png
```

---

## 🔧 Technologies Used

- **Python 3.x**
- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computations
- **matplotlib & seaborn** - Data visualization
- **yfinance** - Financial data collection
- **scipy** - Statistical analysis

---

## 📥 Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/gold-us10y-analysis.git
cd gold-us10y-analysis
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the Jupyter notebook
```bash
jupyter notebook gold_us10y_analysis.ipynb
```

**Note:** On first run, the notebook will download ~20 years of historical data from Yahoo Finance. Subsequent runs will load from the saved CSV file for faster execution.

---

## 📈 Key Findings

### Overall Relationship
- **Correlation:** Moderate negative correlation observed (varies by period)
- **Interpretation:** The classical theory holds partially - when yields rise, gold prices tend to fall, but the relationship is not constant

### Time-Varying Dynamics
- The correlation is **not stable** over time
- Different economic regimes show drastically different relationships
- Crisis periods (2008, COVID) show different patterns than stable periods

### Period-Specific Insights

| Period | Correlation | Key Characteristics |
|--------|-------------|---------------------|
| **Pre-2008 Crisis** | Variable | Relatively stable relationship |
| **2008 Crisis Era** | Weakened | Flight to safety dominates |
| **Post-Crisis Recovery** | Moderate negative | QE impacts both assets |
| **COVID Era** | Disrupted | Unprecedented monetary policy |
| **Fed Tightening (2022+)** | Strengthening | Classical relationship returns |

### Key Takeaways
✅ Rising yields DO tend to pressure gold prices, but...  
⚠️ The relationship breaks down during crises  
⚠️ Other factors (dollar strength, inflation, geopolitics) matter significantly  
⚠️ Not a simple causation - correlation varies across time periods  

---

## 📊 Visualizations

The analysis generates 7 key visualizations:

1. **Time Series Plot** - Dual-axis view of gold and yields over 20 years
2. **Scatter Plot** - Relationship with regression line and R² value
3. **Distribution Analysis** - Statistical properties of both variables
4. **Rolling Correlation** - How correlation evolves over time
5. **Period Comparison** - Side-by-side analysis across economic regimes
6. **Final Summary** - Comprehensive 4-panel overview
7. **Additional charts** - Supporting analysis

---

## 🔍 Methodology

### Data Collection
- **Gold Prices:** Gold Futures (GC=F) from Yahoo Finance
- **Treasury Yields:** 10-Year Treasury Yield Index (^TNX) from Yahoo Finance
- **Time Period:** November 2004 - October 2025 (~20 years)
- **Frequency:** Daily observations

### Analysis Techniques
1. **Correlation Analysis** - Pearson correlation coefficient
2. **Regression Analysis** - Linear regression with statistical tests
3. **Rolling Window Analysis** - 90-day, 180-day, and 365-day windows
4. **Period Segmentation** - Analysis across 5 distinct economic periods
5. **Visual Exploration** - Multiple visualization techniques

### Data Quality
- Missing values handled via forward/backward fill
- Datasets merged on date with inner join
- Final clean dataset with ~5,000+ observations

---

## ⚠️ Limitations

- **Correlation ≠ Causation:** Analysis shows association, not causal relationship
- **Omitted Variables:** Dollar strength (DXY), inflation expectations, VIX not included
- **Linear Assumption:** Relationship may be non-linear
- **No Lag Analysis:** Doesn't examine if yields lead or lag gold prices
- **Regime Changes:** Structural breaks not formally tested

---

## 🚀 Future Enhancements

- [ ] Granger causality test (does yield predict gold movements?)
- [ ] Include control variables (DXY, VIX, inflation expectations)
- [ ] Vector Autoregression (VAR) model
- [ ] Analysis of percentage changes vs levels
- [ ] Structural break detection
- [ ] Machine learning models for prediction
- [ ] Interactive dashboard (Plotly/Dash)

---

## 📚 References

- **Data Source:** [Yahoo Finance](https://finance.yahoo.com/)
- **Economic Theory:** Opportunity cost of holding non-yielding assets
- **Related Research:** Literature on gold as safe haven vs inflation hedge

---

## 👤 Author

**[Your Name]**
- GitHub: [@yourusername](https://github.com/yourusername)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/yourprofile)
- Email: your.email@example.com

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Yahoo Finance for providing free historical financial data
- The Python data science community for excellent open-source tools
- Economic literature on gold and bond market relationships

---

## 📞 Contact

For questions, suggestions, or collaboration opportunities, feel free to:
- Open an issue on GitHub
- Reach out via LinkedIn
- Send an email

---

**⭐ If you found this analysis helpful, please star the repository!**