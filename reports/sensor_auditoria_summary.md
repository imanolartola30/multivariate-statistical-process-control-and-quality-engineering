| Step                                        |   Sensors_Removed |   Sensors_Remaining | Reason                                                   |
|:--------------------------------------------|------------------:|--------------------:|:---------------------------------------------------------|
| 1. Initial Raw Sensors                      |                 0 |                 590 | Raw SECOM telemetry input                                |
| 2. Missing Data Filter (>40% NaN)           |                28 |                 562 | Unreliable / sparse sampling in Phase I                  |
| 3. Zero-Variance Filter (std < 1e-6)        |               122 |                 440 | Constant / turned-off sensors                            |
| 4. Extreme Collinearity Filter (|r| > 0.98) |               126 |                 314 | Redundant channels (prevents singular covariance matrix) |