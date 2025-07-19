# 📊 Data & Model Analysis Report

## 🧾 1. Dataset Description

- The dataset includes JSON logs from Aave V2 protocol events.
- Each record contains:
  - `wallet`: User wallet address
  - `network`: Blockchain network
  - `action`: Type of DeFi action (borrow, repay, etc.)
  - `amount`, `assetPriceUSD`: Value-based features
  - Timestamps, transaction hashes, and reserve IDs

## 🔎 2. Data Preprocessing

- Extracted fields from nested JSON (e.g., `actiondata.amount`, `collateralAmount`)
- Cleaned data types, removed nulls, and standardized formatting.
- Aggregated data at wallet level:
  - Total borrowed amount
  - Count of borrow/repay/liquidation actions
  - Average asset price, etc.

## 📐 3. Feature Engineering

- Created new features like:
  - `borrow_ratio = total_borrow / (total_borrow + total_repay)`
  - `liquidation_flag`: 1 if ever liquidated, else 0
- Labeled wallets as:
  - High Risk (Score: 2)
  - Medium Risk (Score: 1)
  - Low Risk (Score: 0)

## 🤖 4. Machine Learning

- Model: RandomForestClassifier
- Train/Test Split: 80/20
- Accuracy: ~92%
- Classification Report:
