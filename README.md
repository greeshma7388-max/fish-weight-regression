# Predicting Fish Weight Using Regression Models

Regression analysis comparing three model classes for predicting 
freshwater fish weight from morphological measurements.

## Dataset
Fish Market Dataset — 159 fish across 7 Northern European freshwater 
species (Bream, Parkki, Perch, Pike, Roach, Smelt, Whitefish)  
Source: NCI Statistics and Optimisation Module, 2026

## Models Compared
| Model | R² | RMSE (g) |
|---|---|---|
| Multiple Linear Regression | 0.912 | 140.28 |
| Linear with Species Interactions | 0.971 | 80.25 |
| Log-Linear (Logarithmic) | **0.996** | **44.23** |

## Key Insights
- Log-linear model reduced RMSE by 69% vs linear baseline
- Biological allometric power law (W ∝ L³) guided model selection
- VIF screening identified and resolved extreme multicollinearity 
  across three length variables (VIF > 100)
- Duan smearing correction applied for log-space back-transformation
- Best model predicts a Perch (L=41.9cm, H=12.8cm, W=6.9cm) 
  at 640.73g

## Tools & Libraries
Python · Statsmodels · Pandas · Matplotlib · Seaborn · NumPy

## Project Structure
fish_regression.py     # Full pipeline: EDA, VIF, 3 models, diagnostics
