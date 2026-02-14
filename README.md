# Sports Betting Arbitrage Detection

This project analyzes sports betting markets to identify arbitrage opportunities across different sportsbooks. The goal is to detect risk-free profit scenarios when implied probabilities across books create a pricing inefficiency.

---

## Overview

This notebook:

- Imports sportsbook odds data
- Converts odds into implied probabilities
- Calculates overround (bookmaker margin)
- Identifies arbitrage opportunities
- Computes optimal stake allocation
- Calculates guaranteed profit margins

The analysis demonstrates how pricing discrepancies across books can be systematically exploited using quantitative methods.

---

## Arbitrage Concept

An arbitrage opportunity exists when:

Sum of implied probabilities < 1

When this condition is met, it is possible to allocate capital across all outcomes and guarantee profit regardless of the event result.

Mathematically:

```
1 / Odds_A + 1 / Odds_B + ... < 1
```

If true, a risk-free return is achievable.

---

## Methods

### 1. Odds Conversion
Odds (decimal or American) are converted into implied probabilities:

```
Implied Probability = 1 / Decimal Odds
```

### 2. Arbitrage Detection
The script checks:

```
Total Implied Probability < 1
```

If satisfied, an arbitrage flag is triggered.

### 3. Stake Allocation
Capital is distributed proportionally:

```
Stake_i = Total Bankroll × (Implied Probability_i / Total Implied Probability)
```

This ensures equalized payout across all outcomes.

### 4. Profit Calculation
Guaranteed return is computed as:

```
Profit = Total Payout − Total Stake
```

---

## Technologies Used

- Python
- pandas
- numpy
- matplotlib (if visualization included)

---

## How to Run

1. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib
   ```

2. Run the Jupyter notebook:
   ```bash
   jupyter notebook Sports_Betting_ARB.ipynb
   ```

---

## Key Takeaways

This project demonstrates:

- Understanding of implied probability and bookmaker margin
- Detection of pricing inefficiencies
- Risk-free portfolio allocation logic
- Practical quantitative strategy implementation
- Applied probability and financial math in betting markets

---

## Potential Extensions

- Multi-book automated scraping
- Real-time arbitrage detection
- Transaction cost modeling
- Capital constraints optimization
- Kelly-criterion integration
- API integration with sportsbooks

---

**Author:** Miles Choquette  
M.S. Quantitative Finance | Computer Science Background
