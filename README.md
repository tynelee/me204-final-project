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

The notebooks should be run in order from `NB01-Data-Collection.ipynb` to `NB02-Data-Transformation.ipynb` to `NB03-tynelee-Data-Analysis.ipynb`, and:

1. Make sure python 3+ is installed
2. Install these packages on your python environment:

    ```shell
    pip install python-dotenv requests pandas plotly kaleido
    ```

## Findings

Across all 712 matches, players who won typically had a slight edge in extra winners hit (7 more than their opponent) over a reduction in errors (6 less than their opponent), but neither style shows a significant edge over the other (`NB03-tynelee-Data-Analysis.ipynb` fig1).

Splitting by surface shows a predictable shift, on hard courts and grass, aggression is rewarded, while this is tempered on clay, the surface of patience and grit (`NB03-tynelee-Data-Analysis.ipynb` fig2).

The most notable finding comes when serve statistics are removed, to isolate rally play from raw serving. The winners margin becomes noticeably compressed, suggesting that a meaningful amount of reward for being aggressive is really an advantage of serving, not rally-based risk taking. Once serving was accounted for, the two playing styles looked a lot more balanced (`NB03-tynelee-Data-Analysis.ipynb` fig1_rally & fig2_rally).

