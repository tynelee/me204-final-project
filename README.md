# ME204 Final Project: How Deterministic Is Rally Length for Winning Matches? Evidence from the ATP Finals


| GitHub username                           | LSE ID            |
| ----------------------------------------- | ----------------- |
| `Tyne Lee`                              | `250099310`        |


## Overview

This project asks whether winning short rallies (0-4 shots) is more decisive than winning long rallies (9+ shots), using rally analysis data from the 2022-2024 ATP finals. Rally length can be used to infer things about playing style and risk tolerance, so it offers a way to test whether one way of point-winning matters more than the other.

## Data sources

The main source used for this project was rally analysis data and general match information scraped via the Infotennis Github (https://github.com/glad94/infotennis) package, which retrieves data from ATP's public Infosys-powered stats API. 

## How to reproduce

[Tell your reader how to get keys, which python commands to run and any other things they need to know when replicating your work (imagine they are people with similar technical skills as yours)]

The notebooks should be run in order from `NB01-Data-Collection.ipynb` to `NB02-Data-Transformation.ipynb` to `NB03-tynelee-Data-Analysis.ipynb`, and the following packages must be installed:

1. Make sure you have python 3+ installed
2. Install these packages on your python environment:

    ```shell
    pip install plotly pandas
    ```

3. Clone the Infotennis repository to the local machine and install with pip:

    ```
    $ git clone https://github.com/glad94/infotennis
    $ cd infotennis
    $ pip install .
    ```


***SQL?

