# Cause of College Alcohol Consumption — ML Analysis

## Overview
A machine learning study exploring which factors have the greatest 
effect on alcohol consumption among college students. Rather than 
just predicting alcohol consumption, the goal was to figure out 
which factors play the biggest role by systematically removing 
columns from the dataset and measuring the effect on model accuracy.

## Methods
Four machine learning models were tested and compared:
- K-Nearest Neighbors (KNN)
- Weighted KNN
- Decision Tree
- Random Forest

The dataset was tested with all columns included, then each column 
was removed one at a time to see how much it affected average model 
accuracy. This produced a final visualization showing which columns 
had the highest correlation with alcohol consumption.

## Results
The column `goout, which rates how much students go out with 
friends on a scale of 1-5, produced the largest drop in accuracy 
when removed, suggesting it has the highest correlation with alcohol 
consumption. This makes sense as alcohol consumption is a social 
activity. Age and sex also showed high positive differences in 
average accuracy, which also makes sense as people tend to drink 
more as they get older, and body mass differences between men and 
women affect alcohol tolerance.

Interestingly, health and absences had a negative difference in 
accuracy, meaning models actually performed better without them. 
This was unexpected since drinking is bad for health and could 
cause absences due to things like hangovers, but the data did not 
show strong correlation for either.

Random Forest and Decision Tree performed much better than KNN and 
weighted KNN, likely due to the large number of binary columns in 
the dataset which work better with tree-based models.

## Future Work
- Use only Random Forest or Decision Tree accuracy instead of 
  averaging all models, which would produce a more accurate final 
  visualization
- Test using weekday alcohol consumption as the target variable 
  instead of weekend consumption to see how results change

## Technologies
- Python
- scikit-learn
- pandas
- Google Colab
