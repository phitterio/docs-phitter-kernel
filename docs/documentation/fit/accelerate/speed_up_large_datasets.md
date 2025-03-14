# Speed up for large datasets

To speed up the fit for large amount of data, **Phitter** provides two strategies:

- **_Strategy 1_**: Specify a sample size smaller than the original dataset. A sample size of less than 100K is suggested. Phitter will randomly select a subsample of the specified size. To use this strategy you should use the parameter `subsample_size` explain in [Create Continuous Fit](/documentation/fit/continuous/create_continuous.md) or [Create Discrete Fit](/documentation/fit/discrete/create_discrete.md)

- **_Strategy 2_**: Specify an estimation sample size smaller than the original dataset. A sample size of less than 10K is suggested. Phitter will randomly select a subsample of the specified size for parameter estimation. To use this strategy you should use the parameter `subsample_estimation_size` explain in [Create Continuous Fit](/documentation/fit/continuous/create_continuous.md) or [Create Discrete Fit](/documentation/fit/discrete/create_discrete.md)

::: info
You can use either one of the above strategies or both.
:::

To use it, create the object with those parameters:

```python
phi = phitter.PHITTER(
    data=data,
    subsample_size=10000,
    subsample_estimation_size=10000,
)
```
