---
title: Lichess Insights Analyzer
emoji: ♟️📊
colorFrom: blue
colorTo: green
sdk: streamlit
app_file: app.py
pinned: false
license: apache-2.0
---

# Lichess Insights Analyzer ♟️📊

Dive deep into your Lichess chess game statistics! This Streamlit web application analyzes your rated Bullet, Blitz, and Rapid games directly from the Lichess API.

**Key difference from the original Kaggle notebook:** While the notebook analyzed pre-downloaded data for Alireza Firouzja, this web app allows you to **analyze the games of *any* Lichess user** simply by entering their username!

**🚀 Try the live app here:** https://huggingface.co/spaces/Andolinism/lichess-insights


## ✨ Features / Analysis Sections

Explore various aspects of any Lichess user's performance, including:

*   **Overview & General Stats:** Win rate, total games, W/L/D ratio, average opponent Elo.
*   **Performance Over Time:** Rating trend, games per year, win rate per year.
*   **Performance by Color:** Detailed win/loss/draw percentages for White and Black.
*   **Time & Date Analysis:** Performance based on day of the week, hour of the day (UTC), and day of the month. Includes time control category breakdown.
*   **ECO & Opening Analysis:** Frequency and win rates for openings, presented using both standard Lichess API naming and a custom ECO code mapping (from `eco_to_opening.csv`).
*   **Opponent Analysis:** Most frequent opponents and performance based on Elo difference against the field.
*   **Games against Titled Players:** Filter and analyze performance specifically against players with official FIDE titles (GM, IM, FM, CM, WGM, WIM, WFM, WCM, NM).
*   **Termination Analysis:** Breakdown of game endings, including a detailed analysis of wins and losses due to time forfeits, broken down by time control.

## 🎮 How to Use

1.  Navigate to the app using the link above: https://huggingface.co/spaces/Andolinism/lichess-insights
2.  Enter the **Lichess Username** you want to analyze in the sidebar settings.
3.  Select the **Time Period** for the analysis.
4.  Choose the **Game Type** (Bullet, Blitz, or Rapid).
5.  Click the **"Analyze Games"** button.
6.  Wait for the data to be fetched and processed.
7.  Explore the analysis sections using the sidebar.
8.  Interact with the plots (hover, use modebar buttons). *Direct drag-to-zoom is disabled for better mobile scrolling.*

## 🛠️ Technology Stack

*   **Language:** Python
*   **Web Framework:** Streamlit
*   **Data Manipulation:** Pandas
*   **Plotting:** Plotly
*   **API Interaction:** Requests
*   **Hosting:** Hugging Face Spaces

## 💾 Data Source

*   Game data is fetched directly from the [Lichess API](https://lichess.org/api) based on the provided username and filters.
*   Custom opening name mapping uses the `eco_to_opening.csv` file.

## 🙏 Acknowledgements

This web application is heavily inspired by and expands upon the analysis performed in the Kaggle notebook:
[Chess Insights: Alireza Firouzja's Games Analysis](https://www.kaggle.com/code/mynameiskaveh/chess-insights-alireza-firouzja-s-games-analysis) by [mynameiskaveh](https://www.kaggle.com/mynameiskaveh).

## 📜 License

This project is licensed under the Apache 2.0 License (or the license you selected).
