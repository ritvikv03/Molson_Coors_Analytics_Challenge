# Molson Coors Analytics Challenge: eCommerce Content Optimization

## Overview

This repository contains a comprehensive data analytics project that addresses a critical business question in the beer industry: **"What types of content on eCommerce sites are most effective for driving online beer sales?"**

The analysis reveals a counterintuitive finding: **Facts > Feelings**. Information density and numeric facts positively correlate with eCommerce performance, while emotional sentiment and flowery descriptions negatively correlate with sales.

## Key Findings

### Statistical Insights

| Metric | Correlation | Impact |
|--------|-------------|---------|
| **Occasion Mentions** | -0.524 | Most negative impact on sales |
| **Taste Descriptors** | -0.425 | Emotional language hurts performance |
| **Readability Score** | +0.483 | Easier-to-read copy improves sales |
| **Sentiment Score** | -0.308 | Negative correlation with sales |
| **Numeric Facts** | +0.181 | Positive correlation with sales |

### Case Study: Coors Light vs Bud Light

Coors Light outperforms Bud Light by **42.9%** in eCommerce sales (0.70 vs 0.49 index), driven by:

- **3 numeric facts** (ABV, calories, carbs) vs 0 for Bud Light
- **Shorter sentences**: 11 words/sentence vs 18 words/sentence
- **Structured technical language** vs emotional/flowery descriptions

### Top 3 Optimization Recommendations

1. **Add Numeric Facts** (Priority #1)
   - Include ABV%, calories, carbs, serving size
   - Place in first 2 sentences for AI visibility

2. **Shorten Sentences** (Target: 11-15 words)
   - Break complex descriptions into simple statements
   - One key fact per sentence

3. **Use Specific Technical Language**
   - Replace vague terms with precise descriptions
   - Optimize for AI semantic search (ChatGPT, Perplexity, Google AI Overviews)

**Expected Impact:** 30-40% increase in eCommerce sales based on comparative analysis

## Dataset

- **Source:** Kroger.com (major eCommerce retailer)
- **Collection Date:** January 2025
- **Sample Size:** 12 beer/seltzer brands
- **Brands Analyzed:** White Claw (2 variants), Miller Lite, Busch Lite, Michelob Ultra, Coors Light, Coors Banquet, Bud Light, Budweiser, Corona Extra, Pacifico Clara, Modelo Especial

## Methodology

### 1. Data Collection
- Manual collection from Kroger.com with validation
- Includes automated web scraping code for future scaling
- Documentation of data extraction best practices

### 2. NLP Metrics Calculation (15+ Features)

**Sentiment Analysis:**
- VADER sentiment analyzer (compound, positive, negative, neutral scores)

**Text Complexity:**
- Sentence count, average sentence length, average word length
- Lexical diversity, readability scores
- Flesch Reading Ease, Flesch-Kincaid Grade Level

**Content Features:**
- Numeric facts count
- Brewing details mentions
- Taste descriptors frequency
- Occasion mentions
- Information density (facts per sentence)
- Keyword density
- Brand mention frequency

### 3. Statistical Analysis
- Pearson correlation between metrics and eCommerce sales index
- P-value significance testing
- Bootstrap confidence intervals
- Sample size limitations acknowledged (n=12)

### 4. Gen AI Search Optimization
- Analysis of AI-powered search evolution (ChatGPT, Perplexity, Claude)
- Retrieval-Augmented Generation (RAG) architecture explanation
- Platform-specific optimization strategies
- Content optimization framework for AI visibility

## Visualizations

The notebook generates 7 professional presentation-ready charts:

1. **eCommerce Sales Performance Ranking** - Comparative sales index by brand
2. **Information Density vs Sales** - Bubble chart with trend analysis
3. **Sentiment vs Sales** - Scatter plot showing weak correlation
4. **NLP Metrics Correlation Analysis** - Comprehensive heatmap visualization
5. **Coors Light vs Bud Light Comparison** - Side-by-side metric comparison
6. **Content Optimization Priority Ranking** - Implementation priority guide
7. **Key Metrics Dashboard** - Summary cards with optimal values

## Repository Structure

```
Molson_Coors_Analytics_Challenge/
│
├── MolsonCoors1_0_0.ipynb          # Main analysis notebook
├── Coors Light vs. Bud Light (1).pdf  # Supporting documentation
└── README.md                        # This file
```

## Requirements

```python
# Core Libraries
pandas
numpy
matplotlib
seaborn

# NLP & Text Analysis
nltk
vaderSentiment
beautifulsoup4
requests
textstat

# Statistical Analysis
scipy
```

## Usage

### Running the Analysis

1. Clone the repository:
```bash
git clone https://github.com/ritvikv03/Molson_Coors_Analytics_Challenge.git
cd Molson_Coors_Analytics_Challenge
```

2. Install required packages:
```bash
pip install pandas numpy matplotlib seaborn nltk vaderSentiment beautifulsoup4 requests textstat scipy
```

3. Download NLTK data:
```python
import nltk
nltk.download('vader_lexicon')
nltk.download('punkt')
```

4. Open and run the Jupyter notebook:
```bash
jupyter notebook MolsonCoors1_0_0.ipynb
```

### Key Outputs

- **Correlation analysis** of 15+ NLP metrics vs sales performance
- **Statistical significance testing** with p-values
- **Actionable recommendations** for content optimization
- **Presentation-ready visualizations** for stakeholder communication

## Future Work

### Phase 1: Extended Research (Month 1-2)
- Expand to 50+ beer brands across multiple retailers
- Include seasonal variations and regional differences
- Validate findings with larger sample size

### Phase 2: A/B Testing Framework (Month 2-3)
- Design controlled experiments for Molson Coors brands
- Test optimized copy variants
- Measure lift in conversion rates

### Phase 3: ML Prediction Models (Month 3)
- Build regression models to predict sales from copy features
- Create content scoring algorithm
- Develop automated optimization tool

### Success Metrics
- 30-40% increase in eCommerce sales
- Improved AI search ranking
- Higher conversion rates from AI recommendations
- ROI: 5-10x return on content optimization investment

## Applications

This analysis framework can be applied to:
- **Product Description Optimization** for eCommerce platforms
- **AI Search Visibility** for ChatGPT, Perplexity, Google AI Overviews
- **Content Strategy Development** for digital marketing
- **Competitive Analysis** of market positioning
- **A/B Testing** content variants

## Author

**Ritvik Vasikarla**

## License

This project is part of the Molson Coors Analytics Challenge.

## Acknowledgments

- Data source: Kroger.com
- NLP tools: NLTK, VADER Sentiment Analyzer
- Statistical analysis: SciPy, NumPy
- Visualization: Matplotlib, Seaborn

---

**Note:** This analysis is based on a sample of 12 brands from January 2025. While correlations show promising patterns, expanded research with larger sample sizes is recommended for definitive conclusions.
