# Detroit Tigers 2025 Starter Performance Analysis

## Project Overview

This project analyzes the 2025 season of the Detroit Tigers to answer the following question:

### What was the Tigers' record in games where the starting pitcher threw 6 or more innings?

The goal of this project is twofold:

1. Build foundational skills in baseball data extraction and cleaning using Python.
2. Develop a structured, repeatable analytics workflow similar to what might be used in a baseball operations environment.

This project represents my first structured baseball analytics analysis.

## Why This Question?

Starting pitcher workload has significant implications for:

- Bullpen usage
- Run prevention
- Game outcomes
- Long-term roster strategy

By examining team performance when a starter pitches at least 6 innings, we can begin exploring the relationship between starting pitcher durability and winning percentage.

This project focuses on process over complexity - building the pipeline correctly before adding advanced metrics.

## Tools and Libraries Used

- Python
- Pandas
- Pybaseball
- Git/Github

## Data Sources

Data was pulled programmatically using the pybaseball library, which aggregates publicly available MLB data sources such as:

- Baseball reference
- FanGraphs

All data is retrieved via Python scripts - no manual CSV downloads.

## Methodology

1. Retrieve 2025 Detroit Tigers Schedule
   Pulled full season game results
2. Retrieve 2025 pitcher game logs
   Filtered to:

- Team = DET
- Games Started (GS) = 1

3. Clean innings pitches
   Handled baseball's fractional inning format (e.g., 6.1, 6.2)
4. Filter condition
   Selected games where:

- Innings Pitched >= 6.0

5. Merge with game outcomes
   Joined pitching logs with team win/loss results by date
6. Compute record
   Calculated total wins and losses in qualifying games.

## Key Skills Demonstrated

- API-based data extraction
- Data cleaning and type conversion
- Filtering and role identification (starter vs reliever)
- Dataset merging
- Aggregation and record calculation
- Reproducible workflow design

## Next Steps / Extensions

Future expansions of this project may include:

- Comparing record when starters go < 6 innings
- Analyzing bullpen ERA in short-start games
- Examining run differential
- Comparing Tigers results to league average
- Incorporating advanced pitching metrics (xERA, FIP, SIERA)

## Long-Term Development Goal

The objective is to build increasingly advanced models and analyses over time, with a long-term goal of contributing to a Major League Baseball front office.
