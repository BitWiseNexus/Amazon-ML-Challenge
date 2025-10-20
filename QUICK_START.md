# Quick Start Guide - Improved Model

## Steps to Generate Improved Predictions

### Option 1: Run All New Cells (Recommended)
1. Scroll down to the section: **"# IMPROVED MODEL - Advanced Feature Engineering & Ensemble Methods"**
2. Run all cells from that section onwards
3. Wait for training to complete (15-30 minutes depending on your machine)
4. Find your submission file: `test_out_improved.csv`

### Option 2: Run Cell by Cell
Execute in order:
1. Install packages (xgboost, catboost)
2. Import libraries
3. Reload data
4. Extract advanced features
5. Compute price per unit
6. Add brand statistics
7. Add unit statistics
8. Create TF-IDF features
9. Prepare feature matrix
10. Split data
11. Train LightGBM
12. Train XGBoost
13. Train CatBoost
14. Evaluate models
15. Create ensemble
16. Train final models
17. Generate predictions
18. Save submission

## What's Different?

### Features (513 → 1030)
- ✅ Brand target encoding (mean, median, std, count)
- ✅ Unit target encoding (mean, median, count)
- ✅ Category indicators (food, electronics, health, home)
- ✅ Size indicators (ounce, pound, gram, liter, count)
- ✅ Text quality features
- ✅ More TF-IDF features (500 → 1000)

### Models (1 → 3)
- ✅ LightGBM (optimized)
- ✅ XGBoost
- ✅ CatBoost
- ✅ Weighted ensemble

## Expected Results

### Validation Performance
- Individual models: ~30-35% SMAPE each
- Ensemble: ~28-35% SMAPE
- **Improvement: 15-25% over baseline**

### Test Performance
- Expected: **< 40% SMAPE** ✅
- Target: **< 40% SMAPE** ✅

## Troubleshooting

### If cells fail:
1. Make sure you're in the correct directory with `train.csv` and `test.csv`
2. Install missing packages: `pip install xgboost catboost`
3. Check memory usage - ensemble needs ~8GB RAM

### If score is still > 40%:
1. Try different ensemble weights
2. Add more sophisticated features
3. Use stacking instead of weighted average
4. Try different hyperparameters
5. Remove outliers from training data

## Time Estimates
- Feature extraction: 5-10 minutes
- Model training: 10-20 minutes
- Total: 15-30 minutes

## Output Files
- `test_out_improved.csv` - Your submission file
- This is ready to submit to the competition portal
