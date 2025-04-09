# Delay Cournot Duopoly Model (Mathematica)

This repository contains a dynamic Cournot duopoly model implemented in Wolfram Mathematica. The model includes **memory dynamics** using exponential smoothing, where firms respond not only to current outputs but also to smoothed past outputs.

## Model Description

Two firms compete by choosing output levels. Their decisions are influenced by:

- Their own past output (memory term)
- The competitor’s past output
- The time delay is modeled via exponential smoothing with delay parameter `T`

### Differential System

The system includes:
- Evolution equations for `x(t)` and `y(t)` (output levels)
- Delay equations for `xd(t)` and `yd(t)` (smoothed memory variables)

### Parameters

- `T` — delay (varies from 1 to 10)
- `a`, `b`, `c1`, `c2`, `al`, `be` — model constants

## Features

- `ParametricNDSolve` is used to solve the system for multiple values of delay `T`
- Time series plots for x(t) and y(t)
- Color-coded legend by delay values

## Output

- `px` — plot of `x(t)` for T = 1 to 10
- `py` — plot of `y(t)` with legend by delay τ

## Usage

1. Open `main_code.m` in Wolfram Mathematica.
2. Define parameters `a`, `b`, `c1`, `c2`, `al`, `be`.
3. Run the script to simulate and visualize the system.

## License

MIT License
