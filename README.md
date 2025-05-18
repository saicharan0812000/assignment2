# Assignment 2 – Data Cleaning and Analysis

**Student Name:** Sai Charan Pokuri  
**Student ID:** 23980376

## Overview

This assignment focuses on preprocessing a dataset of board games and performing statistical analysis on it using shell scripting and `awk`.

---

## Files

### `preprocess`
- **Input:** A `;`-separated raw dataset file (e.g., `sample.txt`).
- **Output:** A cleaned `.tsv` file with the same base name.
- **Functionality:**
  - Converts `;` to tab (`\t`).
  - Replaces commas in numeric fields with dots.
  - Removes non-ASCII characters.
  - Fills missing IDs in column 1 with unique values.

### `analysis`
- **Input:** A cleaned `.tsv` file (e.g., `sample.tsv`).
- **Output:** Correlation values and frequency counts.
- **Functionality:**
  - Computes Pearson correlation between:
    - Year Published and Rating Average.
    - Complexity Average and Rating Average.
  - Finds the most common:
    - Game mechanic.
    - Game domain.

### `empty_cells`
- **Input:** A raw dataset file and a delimiter (e.g., `;`).
- **Output:** Lists columns and number of empty cells.
- **Usage:** `./empty_cells bgg_dataset.txt ';'`

---

## How to Use

### 1. Clean the data:
```bash
./preprocess sample.txt
