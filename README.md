ASYM_T - Asymmetric Fat-Tailed Distribution Framework


Files:

ASHM_T_PUB.xlsx      -- spreadsheet implementing asymmetric fat-tailed distribution

LAMBDA_DECK_1_v2.pdf --  Presentation: LAMBDA Concepts and Context

LAMBDA_DECK_2_v2.pdf --  Presentation: Prachtical LAMDA Programming


Overview

This spreadsheet implements a configurable asymmetric fat-tailed distribution and applies it to:

* Statistical moment analysis

It demonstrates the use of this distribution in option pricing

* Simulation and numerical integration
* Risk-neutral modeling
* Option pricing

The goal is to demonstrate how non-normal distributions can be used in a fully arbitrage-free pricing framework.


LAMBDA Framework

All logic is implemented using Excel LAMBDA functions.

A full listing of the Excel LAMBDA functions used can be found on a GitHub Gist.

https://gist.github.com/3sigmalectures-ctrl/878ef58edfb1a3730b82af11293d8d3f

Numerical Integration Approach

The model uses inverse CDF discretisation:

u = evenly spaced grid in (0,1)
x = F_inverse(u)

This produces a deterministic approximation of expectations.


Important Observation (Kurtosis)

Excess kurtosis may appear to increase as the number of grid points increases.

This is a numerical artifact:

Finer grids capture more extreme tail values.
Since kurtosis is highly sensitive to tail behaviour, the estimate increases as tail resolution improves.



Limitations

* Numerical results depend on grid resolution
* Kurtosis sensitive to tail truncation
* NOT optimized for very large grids (intended as a learning tool)



Disclaimer

This model is for educational and research purposes only.
It is not investment, trading, accounting, legal, or financial advice.
Use at your own risk.


Author

Leonard Brown
Independent Researcher
3sigmalectures@gmail.com



Acknowledgment

This work was developed with the assistance of OpenAI ChatGPT (GPT-5.3).
All design decisions and implementation are the responsibility of the author.



License

Free to use, modify, and distribute.
Provided “as is” without warranty.


