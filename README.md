# Video Game Sales Analysis with Pandas

**Author:** Shubham Gajjar  
**Date:** November 29, 2025

A comprehensive data analysis project exploring video game sales data spanning multiple decades, platforms, and genres using Python and Pandas.

## Overview

This project performs an in-depth analysis of video game sales data to uncover insights about the gaming industry, including:

- Sales trends across different platforms and genres
- Regional preferences and market differences
- Publisher strategies and performance
- Correlation between game ratings and sales
- Industry evolution from the 1980s to 2020s

## Dataset

The analysis uses two CSV files:

1. **video_games.csv** - Main dataset containing:

   - Game names, platforms, release years
   - Genres and publishers
   - Regional sales (North America, Europe, Japan, Other)
   - Global sales figures
   - **Original size:** 810 rows, 10 columns
   - **After cleaning:** 738 rows, 10 columns

2. **game_ratings.csv** - Ratings dataset containing:
   - Game names and platforms
   - Critic scores (Metacritic, 0-100)
   - User scores (0-10)
   - ESRB ratings
   - **Original size:** 494 rows, 5 columns
   - **After cleaning:** 485 rows, 5 columns

## Project Structure

The analysis is organized into four main parts:

### Part 1: Data Loading and Cleaning (12 points)

- Loading and initial exploration of datasets
- Handling missing values (Year, Publisher, User_Score)
- Removing duplicate rows
- Data type conversions and validation
- Verifying data integrity (Global_Sales = sum of regional sales)

**Key Cleaning Steps:**

- Removed 72 rows from games dataset (missing Year/Publisher, duplicates)
- Removed 9 rows from ratings dataset (missing scores, duplicates)
- Converted 'tbd' strings to NaN in User_Score
- Recalculated Global_Sales to match regional sum

### Part 2: Exploratory Data Analysis (12 points)

- **Top Games Analysis:** Best-selling games and publishers
- **Platform Analysis:** Games count, total sales, and average sales per platform
- **Genre Analysis:** Sales performance across different genres
- **Temporal Analysis:** Trends over time (1985-2020)

**Key Findings:**

- Best-selling game: "Adventure" (PS4, 2014) with 83.24M units
- Top publisher: Electronic Arts (167.29M total sales)
- Most games: PS3 platform (87 games)
- Highest sales: PS4 platform (252.07M units)
- Most popular genre: Sports (282.53M total sales)
- Peak year: 2014 (240.64M sales)

### Part 3: Advanced Analysis (16 points)

- **Regional Sales Analysis:** Market distribution and regional preferences
- **Publisher Deep Dive:** Detailed analysis of top 5 publishers
- **Rating Analysis:** Correlation between critic/user scores and sales
- **Feature Engineering:** Created Decade and Sales_Category columns

**Key Insights:**

- North America: 52.69% of global sales
- Europe: 36.80% of global sales
- Japan: 10.51% of global sales
- Critic scores correlation with sales: 0.1467 (weak positive)
- User scores correlation with sales: 0.0433 (very weak)
- Found many "hidden gems" (high scores, low sales) and "overhyped" games (low scores, high sales)

### Part 4: Insights and Open Exploration (10 points)

- **Platform Wars:** Comparison of console generations (PS2/Xbox/GameCube, PS3/Xbox360/Wii, PS4/XboxOne)
- **Publisher Strategy:** Nintendo vs EA comparison
- **Industry Evolution:** Changes from 1980s to 2010s
- **Regional Preferences:** Games successful in one region but not others

**Key Discoveries:**

- PS2 won Generation 6, Wii won Generation 7, PS4 won Generation 8
- EA has higher average sales per game (2.14M) than Nintendo (1.19M)
- Industry grew 15x in game releases from 1980s to 2010s
- Sales grew 125x from 1980s (6.32M) to 2010s (802.12M)
- Many Western action/shooter games perform poorly in Japan

## Key Statistics

### Dataset Summary

- **Total games analyzed:** 738 (after cleaning)
- **Year range:** 1985-2020
- **Platforms:** 17 unique platforms
- **Genres:** 12 different genres
- **Publishers:** Multiple major publishers

### Sales Distribution

- **Blockbuster games (>5M):** 6.78%
- **Hit games (1-5M):** 20.33%
- **Modest games (<1M):** 72.90%

### Top Performers

- **Best-selling game:** Adventure (PS4, 2014) - 83.24M
- **Top publisher:** Electronic Arts - 167.29M
- **Top platform:** PS4 - 252.07M
- **Top genre:** Sports - 282.53M

## Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical operations
- **Jupyter Notebook** - Interactive analysis environment

## How to Run

1. Ensure you have the required dependencies:

   ```bash
   pip install pandas numpy jupyter
   ```

2. Place the CSV files in the same directory:

   - `video_games.csv`
   - `game_ratings.csv`

3. Open and run the notebook:

   ```bash
   jupyter notebook main.ipynb
   ```

4. Execute all cells sequentially to see the complete analysis

## Files

- `main.ipynb` - Main analysis notebook with all code and results
- `video_games.csv` - Primary dataset
- `game_ratings.csv` - Ratings dataset
- `README.md` - This file

## Key Insights Summary

1. **Market Dominance:** North America accounts for over half of global sales (52.69%)

2. **Platform Success:** PS4 leads in both total sales and average sales per game

3. **Genre Performance:** Sports genre dominates total sales, while Simulation has the highest average sales per game

4. **Rating vs Sales:** Critic and user scores show weak correlation with sales, indicating other factors (marketing, brand, timing) play larger roles

5. **Regional Differences:** Significant cultural preferences exist - many Western action games struggle in Japan

6. **Industry Growth:** Massive expansion from 1980s to 2010s, with both volume and average sales per game increasing dramatically

7. **Publisher Strategies:** EA focuses on volume with Sports franchises, while Nintendo has a more diverse portfolio

## Assignment Requirements

This project fulfills all requirements for the Video Game Sales Analysis assignment:

- ✅ Part 1: Data Loading and Cleaning (12 points)
- ✅ Part 2: Exploratory Data Analysis (12 points)
- ✅ Part 3: Advanced Analysis (16 points)
- ✅ Part 4: Insights and Open Exploration (10 points)

**Total: 50 points**

## Notes

- All data cleaning was performed using Pandas operations (no manual CSV editing)
- Analysis includes proper handling of missing values and data quality issues
- Results are based on the cleaned dataset after removing invalid entries
- The merge operation may create multiple matches for games with same name on different platforms

## License

See LICENSE file for details.
