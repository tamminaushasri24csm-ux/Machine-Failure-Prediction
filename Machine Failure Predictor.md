# ⚙️ Machine Failure Predictor

Predictive maintenance · AI4I 2020 dataset · Cost-Sensitive Random Forest

Checking model…

## Machine readings

Machine quality type

## Prediction

0%

—

**—**Temp difference

**—**Power (W)

**—**Wear × torque

## Likely failure mechanisms

Mechanisms use the AI4I failure definitions (TWF, HDF, PWF, OSF) to explain *why* a reading is risky.

## Model performance (test set, 2,000 records)

| Model | Accuracy | Precision | Recall | F1 |
| --- | --- | --- | --- | --- |
| Logistic Regression | 0.828 | 0.144 | 0.824 | 0.245 |
| Decision Tree | 0.948 | 0.374 | 0.809 | 0.512 |
| Random Forest | 0.985 | 0.932 | 0.603 | 0.732 |
| Cost-Sensitive Random Forest ★ | 0.987 | 0.938 | 0.662 | 0.776 |

## Confusion matrix – selected model

Pred: No

Pred: Fail

Actual: No

**1929**\
correct

**3**\
false alarms

Actual: Fail

**23**\
missed

**45**\
caught

The model catches 45 of 68 real failures with only 3 false alarms. Missed failures are the main weakness, so treat "Low" as "not flagged", not "guaranteed safe".