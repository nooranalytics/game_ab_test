
# Cookie Cats - A/B Testing Analysis

## Introduction

Welcome to the analysis of the popular mobile puzzle game, Cookie Cats. Developed by Tactile Entertainment, Cookie Cats is a classic "connect three"-style puzzle game where the player must connect tiles of the same color to clear the board and win the level. As an added delight, the game features singing cats!
  
As players progress through the levels, they occasionally encounter gates. These gates compel them to wait a significant amount of time or make an in-app purchase to continue. Besides driving in-app purchases, these gates serve an important role - they give players an enforced break, potentially increasing and prolonging their enjoyment of the game.

Our challenge is to decide the optimal placement for these gates. Initially, the first gate was at level 30. However, this repository contains an analysis of an A/B test where we moved the first gate from level 30 to level 40. We will particularly investigate the impact of this move on player retention.


## Data Description

Here's a detailed breakdown of the data under consideration:

- **userid**: A unique identifier for each player.
- **version**: Specifies whether the player was in the control group (gate at level 30) or in the experimental group (gate at level 40).
- **sum_gamerounds**: The total number of game rounds that a player completed during the first week after installation.
- **retention_1**: Indicates whether the player returned to the game 1 day after installation.
- **retention_7**: Indicates whether the player returned to the game 7 days after installation.

 
## Process 

The steps in the analysis provide the following insights:

**Bootstrapping**: Offers a distribution of potential outcomes for the retention rate, assuming that our original sample accurately represents the population. This aids in understanding the variability or uncertainty in our estimate.

**Retention rates for day 1 and 7**: Provides the proportion of players in each group who returned to the game after 1 and 7 days. This is a key metric of user engagement.

**Mean difference**: Reveals the average difference in the retention by the users in the two groups. It helps us gauge the overall impact of shifting the gate on player behavior.

**Probability of superiority**: This reflects the likelihood that retention is higher when the gate is placed at level 30 as compared to a random player from the group where the gate is at level 40. This measure helps us understand the potential impact of gate placement on short-term player engagement.

 **T-test** : Conducted on bootstrapped samples to offer a formal statistical test of the null hypothesis that there's no difference in retention rates between the two groups. This adds to the credibility of our findings.
 
**Segmented Analysis** : This step investigates whether the placement of the gates affected the number of game rounds played.


## How to Run

This analysis is performed in Python, utilizing several popular data science libraries. To run this analysis, you will need to have Python installed on your system, along with the following packages:

- pandas
- numpy
- seaborn
- matplotlib
- scipy

You can install these packages via pip (Python's package manager) by running the following command in your terminal:

```bash
pip install pandas numpy seaborn matplotlib scipy
````


## Data set
https://www.kaggle.com/datasets/yufengsui/mobile-games-ab-testing
