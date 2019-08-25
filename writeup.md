# Writeup

## The effect of the P, I, D component of the PID algorithm

P-value is used to increase the control value proportional to CTE.  
However, the excessively high P-value might cause vibrations.

I-value is effective for Residual Deviation.  
If Residual Deviation remains, the control value gradually increases.

D-value is used for preventing sudden changes.  
When CTE changed quickly, the control value resists the change.

## How I chose the final hyperparameters (P, I, D coefficients)

I set the parameters manually to `(P, I, D)=(0.2, 0.001, 6)`.  
At first, I started from `(0.1, 0.1, 0.1)`.  
Since the amplitude gradually became larger, I decrease I-value to `0.001`.  
Since there was still a small vibration, I gradually increase D-value to `6`.  
After that, the car was able to round almost all of the course, but couldn't turn sharp curves.  
Therefore, I increased P-value to `0.2`.
