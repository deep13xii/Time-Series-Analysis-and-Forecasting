# Sectoral and Market Responses to GST Policy Shocks in India

## Evidence from VARX and QVAR Models

A group project for the **Time Series Analysis and Forecasting** course at the  
**Indian Institute of Science Education and Research (IISER) Bhopal**.

**Authors:**  
- Aswin Jayachandran
- Deep Jangle
- Ishika Goel

**Course:** Time Series Analysis and Forecasting  
**Instructor:** Dr. Biswajit Patra  
**Institution:** IISER Bhopal  
**Project Year:** 2025

---

## Overview

This project investigates how **Goods and Services Tax (GST) policy announcements** affect Indian equity markets, with particular emphasis on sectoral heterogeneity and cross-sector transmission.

The study examines the market response to:

- GST Council meetings
- GST rate-cut announcements
- Associated policy signals and uncertainty

The analysis combines event-based analysis with multivariate time-series techniques to study both **immediate market reactions** and **dynamic transmission across sectors**.

The main empirical framework uses:

- Vector Autoregression with Exogenous Variables (**VARX**)
- Quantile Vector Autoregression (**QVAR**)
- Impulse Response Functions (**IRFs**)
- Forecast Error Variance Decomposition (**FEVD**)
- Quantile connectedness analysis

---

## Research Motivation

While existing research has extensively examined the macroeconomic effects of GST in India, relatively less attention has been given to its **dynamic effects on equity markets and sectoral interconnectedness**.

This project therefore asks:

1. How do GST announcements affect sectoral equity returns?
2. Are the responses homogeneous across sectors?
3. How persistent are GST-related shocks?
4. How do shocks propagate across sectors?
5. What role do uncertainty and market-volatility factors play in sectoral return dynamics?

---

## Data

The study uses daily financial-market data covering the post-GST period.

### Sectoral Indices

The analysis focuses on five NIFTY sectoral indices:

- NIFTY Energy
- NIFTY Pharma
- NIFTY Auto
- NIFTY IT
- NIFTY FMCG

### Control Variables

The models incorporate:

- USD/INR exchange rate
- Economic Policy Uncertainty (EPU)
- India VIX

### GST Policy Variables

Two policy-event indicators are constructed:

- **GST_Meeting** — indicator capturing the GST Council meeting window
- **GST_Cut** — indicator capturing the post-rate-cut period

The project uses daily sectoral returns as the primary market variables.

---

## Methodology

### 1. Event Analysis

The first stage examines sectoral market reactions around GST-related announcements and policy events.

This provides evidence on the immediate and short-run response of sectoral equity returns.

### 2. VARX Model

A **Vector Autoregressive model with Exogenous Variables (VARX)** is used to examine dynamic interactions between sectoral returns while incorporating GST-related policy indicators and control variables.

The VARX framework allows the study to investigate:

- Dynamic sectoral interactions
- Policy-shock transmission
- Persistence of responses
- Cross-sector spillovers

### 3. Impulse Response Functions

**Impulse Response Functions (IRFs)** are used to trace the response of sectoral returns following GST-related shocks.

This helps examine:

- Direction of the response
- Magnitude of the response
- Duration of the response
- Cross-sector transmission

### 4. Forecast Error Variance Decomposition

**FEVD** is used to quantify the contribution of different shocks to the forecast-error variance of sectoral returns.

This provides evidence on the relative importance of:

- Sector-specific shocks
- GST-related policy shocks
- Economic Policy Uncertainty
- Market volatility
- Other system-wide factors

### 5. Quantile VAR and Connectedness

The project extends the analysis beyond conditional-mean relationships using **Quantile VAR (QVAR)**.

Quantile-based analysis allows the study to examine whether relationships differ across different parts of the return distribution.

A connectedness framework is then used to investigate:

- Directional spillovers
- Cross-sector transmission
- Net transmitters and receivers
- Dependence across different market conditions

---

## Research Objectives

The project aims to:

1. Measure the immediate and short-run effects of GST announcements and rate changes on sectoral equity returns.
2. Identify important channels of volatility transmission.
3. Examine cross-sector interconnectedness.
4. Quantify the contribution of different factors to forecast-error variance.
5. Investigate whether GST-related effects differ across the return distribution.

---

## Key Findings

The analysis indicates **heterogeneous responses across sectors** to GST-related policy events.

The study finds evidence that:

- Sectoral equity returns do not respond uniformly to GST policy announcements.
- GST-related shocks can generate short-run movements in sectoral returns.
- The magnitude and persistence of responses vary across sectors.
- Cross-sector interactions play an important role in the transmission of shocks.
- Economic Policy Uncertainty and market-volatility measures contribute to sectoral return dynamics.
- Quantile-based analysis provides additional information about connectedness beyond mean-based relationships.

Overall, the results suggest that the financial-market effects of GST policy are **sector-specific and state-dependent**, rather than uniform across the equity market.

---

## Econometric Workflow

```text
Raw Financial-Market Data
          │
          ▼
     Data Cleaning
          │
          ▼
   Return Construction
          │
          ▼
   Stationarity Tests
       (ADF Test)
          │
          ▼
      Lag Selection
          │
          ▼
      VARX Model
          │
     ┌────┴────┐
     ▼         ▼
    IRF       FEVD
     │         │
     └────┬────┘
          ▼
      QVAR Model
          │
          ▼
 Quantile Connectedness
          │
          ▼
 Sectoral Spillover Analysis
