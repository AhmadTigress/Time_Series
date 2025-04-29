# Challenge Faced During Time Series Forecasting with TIM (Temporal Fusion Transformer)

## Problem
While trying to evaluate my multistep forecasting model using `mean_squared_error` from `scikit-learn`, I encountered the following error:

```
TypeError: got an unexpected keyword argument 'squared'
```

## Root Cause
This happened because the version of `scikit-learn` I was using did not support the `squared=False` argument, which is required to compute RMSE (Root Mean Squared Error) directly. The `squared` parameter was introduced in `scikit-learn v0.22`.

```python
train_rmse = mean_squared_error(y_train, y_fit, squared=False)
test_rmse = mean_squared_error(y_test, y_pred, squared=False)
print((f'Train RMSE: {train_rmse:.2f}\n' f'Test RMSE: {test_rmse:.2f}'))
```

## Solution
To resolve this, I computed the RMSE manually using NumPy, which works across all versions of `scikit-learn`:

```python
from sklearn.metrics import mean_squared_error
import numpy as np

train_rmse = np.sqrt(mean_squared_error(y_train, y_fit))
test_rmse = np.sqrt(mean_squared_error(y_test, y_pred))
print((f'Train RMSE: {train_rmse:.2f}\n' f'Test RMSE: {test_rmse:.2f}'))
```

## Lesson Learned
Always check for version compatibility when using newer parameters or features in popular libraries like `scikit-learn`. It's often safer to implement standard metrics manually if you're unsure of the environment.
