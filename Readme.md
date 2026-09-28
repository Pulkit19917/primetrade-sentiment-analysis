# PrimeTrade: Trader Behavioral & Performance Analysis Across Sentiment Regimes

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Pandas](https://img.shields.io/badge/pandas-data%20analysis-150458.svg)](https://pandas.pydata.org/)
[![Status](https://img.shields.io/badge/status-complete-brightgreen.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **Author:** Pulkit Srivastava  
> **Domain:** Financial Data Engineering, Quantitative Analysis & Behavioral Finance

---

## 📌 Executive Summary

Does market sentiment dictate trader profitability, or do behavioral biases drive structural risk exposure? 

This project investigates account-level trading performance across macro market sentiment regimes—ranging from **Extreme Fear** to **Extreme Greed**. By fusing high-frequency trade logs with daily Fear & Greed index feeds, this framework quantifies how market sentiment influences **PnL distribution, win rates, directional positioning biases (Long/Short), and risk-adjusted efficiency (Sharpe proxy)**.

---

## 🏗️ System Architecture & Data Pipeline

```text
┌────────────────────────┐      ┌────────────────────────┐
│  Fear & Greed Index    │      │ Historical Trade Logs  │
│ (Regime Classification)│      │  (Execution Details)   │
└───────────┬────────────┘      └───────────┬────────────┘
            │                               │
            └───────────────┬───────────────┘
                            ▼
           [ Date Alignment & Normalization ]
                            │
                            ▼
           [ Feature Engineering & Metrics ]
             • Account PnL & Volatility
             • Win Rate & Direction Bias
             • Risk-Adjusted Return (Sharpe Proxy)
                            │
                            ▼
          [ Multi-Dimensional Segmentation ]
             • Volume (High/Low)
             • Frequency (Frequent/Infrequent)
             • Consistency (Low/High Volatility)
                            │
                            ▼
        [ Behavioral & Performance Insights ]
