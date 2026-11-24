# Diamond Price Prediction with Deep Learning
| Metric | Score | Interpretation |
| --- | --- | --- |
| MAE | ~$283.93 | Average price estimate is off by ~$283.93. |
| R2R^2R2 Score | ~0.9804 | Model explains 98%+ of all price variance. |
| MAPE | ~8.24% | Average percentage error across all price tiers. |
| Tolerance (±10%) | ~70.3% | ~70.3% of predictions land within 10% of true market price. |

### Sequential Deep Neural Network (DNN) designed for tabular data:

- Input: 9 standardized features (numerical + ordinal encoded)
- Hidden Layers:
   Dense(128, ReLU) + BatchNormalization + Dropout(0.2)
   Dense(128, ReLU) + BatchNormalization + Dropout(0.2)
   Dense(64, ReLU) + BatchNormalization
- Output: Dense(1) (Linear activation for dollar price)
- Optimization: Adam (lr=0.002) with MAE loss and EarlyStopping
