# A/B Testing: Player Retention for Mobile Game - Cookie Cats

🍪 🐈 🍪 🐈 🍪 🐈

## Context

[Cookie Cats](https://tactilegames.com/cookie-cats/) is a hugely popular mobile
puzzle game developed by [Tactile Entertainment](https://tactilegames.com).
It's a classic "connect three" style puzzle game where the player must connect tiles
of the same color in order to clear the board and win the level.

As players progress through the game they will encounter gates that force them to
wait a set period of time before they can progress or alternatively players can make
an in-app purchase to progress.

An Exploratory Data Analysis and statistical A/B testing data was [performed]
(https://github.com/lorcanrae/ab-test-cookie-cats/blob/master/notebooks/ab-test-cookie-cats.ipynb)
to analyse the impact on the Total Number of Gamerounds played per player, Day 1 Retention and  Day 7 Retention
when the gate was moved from Level 30 to Level 40.

A bootstrap analysis and z-test was performed on the Day 1 and Day 7 Retention.

A bootstrap and Mann-Whitney U test was performed on the number of gamerounds played per player.

It was found that there is adequate evidence to suggest that Day 1 Retention and Day 7 Retention
was higher when the gate is at Level 30. There where no statistically meaningful insights derived
from the number of gamerounds played per player.

<p align='center', float='left'>
  <img src='https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg' width='50'>
  <img src='https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/numpy/numpy-original.svg' width='50'>
  <img src='https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg' width='50'>
  <img src='https://seaborn.pydata.org/_images/logo-mark-lightbg.svg' width='50'>
</p>

## Data

The dataset comes from a [project](datacamp.com/projects/184) on [DataCamp](datacamp.com).

The dataset contains is from 90,189 players that installed the game while the AB Test was running.

Dataset labels:
- `userid` - `int` - unique player identifier.
- `version` - `str` - group the player was randomly assigned to: control (`gate_30` .- gate at Level 30) or treatment (`gate_40` - gate at Level 40).
- `sum_gamerounds` - `int` - total number of rounds completed by the player during the first week after installation.
- `retention_1` - `bool` - `True` if the player played 1 day after installing else `False`.
- `retention_7` - `bool` - `True` if the player played 7 days after installing else `False`.
