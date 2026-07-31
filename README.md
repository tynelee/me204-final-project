# ME204 Final Project: Does Aggression or Consistency Win Tennis Matches?

| GitHub username                           | LSE ID            |
| ----------------------------------------- | ----------------- |
| `Tyne Lee`                                | `250099310`       |

## Overview

This project asks whether reducing unforced errors or hitting more winners is more decisive for winning a tennis match. Winners and unforced errors are two sides of the same coin, and represent two different playing philosophies: aggression vs consistency. So comparing the two can serve as a proxy for identifying whether taking on additional risk pays off at the top level.

## Data sources

The main source used for this project was [API Tennis](https://api-tennis.com/) using the `get_fixtures` endpoint, that returns per-player match statistics (winners, unforced errors, aces, serve percentage etc.) along with general match statistics and context. 

An API key is required, and can be obtained through the free 2 week trial period that API Tennis offers (no credit card details required). The API key must be stored in `.env` as `API_KEY`.

## How to reproduce

Begin by replacing <YOUR_API_KEY_HERE> in the `.env.example` with your own API key from API Tennis. Then rename the file to `.env`. 

The notebooks should be run in order from `NB01-Data-Collection.ipynb` (read API and write `data/raw/dump.json`) to `NB02-Data-Transformation.ipynb` (read `data/raw/dump.json` and process into `data/processed/cleaned.csv`) to `NB03-tynelee-Data-Analysis.ipynb` (read `data/processed/cleaned.csv` and produce plots and analysis).

Ensure the following:

1. Make sure python 3+ is installed
2. Install these packages on your python environment:

    ```shell
    pip install python-dotenv requests pandas plotly kaleido
    ```

