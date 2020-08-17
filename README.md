# Machine Learning and Credit Risk

## Project Overview

Models were tested and trained to evaluate the level of credit risk for loans to individuals based on a variety of factors.

## Resources
#### Language and Packages
* Python v 3.7.6
* NumPy v 1.18.1
* SciPy v 1.4.1
* Scikit-learn v 0.22.1
* imbalanced-learn v 0.7.0
#### Data
* [LoanStats_2019Q1.csv](https://github.com/Alyssa-CG/Module17-Machine_Learning/blob/master/Module-17-Challenge/Resources/LoanStats_2019Q1.csv.zip)
    IMPORTANT: Please note that file was extracted from linked zip to be read into the code as a .csv
    It was only zipped to conform to github size restrictions.


## Summary and Results

Ultimately, credit risk was evaluated by six different means (summary information can be found in [Images](https://github.com/Alyssa-CG/Module17-Machine_Learning/tree/master/Module-17-Challenge/Images)).

The best performer was the model using the Easy Ensemble Classifier (EEC), detailed below.
#### Image of Easy Ensemble Classifier model information
![eec](https://github.com/Alyssa-CG/Module17-Machine_Learning/blob/master/Module-17-Challenge/Images/EasyEnsembleClassifier.png)

This model performed better than the others in multiple areas. 

For one, it has the highest balanced accuracy score at a respectable 0.925 or 92.5%, putting it 13.7% higher than the second most accurate model, the Balanced Random Forest Classifier. This means that 92.5% of the time, this EEC model correctly classifies the risk level of the transactions.

While this model also boasts the highest precision for the high risk category, it remains quite low at 0.07, meaning that it is only 7% likely that a client flagged as high risk is truly high risk.

The recall or sensitiviy of the EEC model is high, at 0.94 for high risk and 0.91 for low risk, indicating that the likelihood of a client being flagged as either high or low risk being truly high or low risk is quite probable. 

The f1 score is also highest for this model, but it is still low for high risk cases, indicating the pronounced imbalance or tradeoff between sensitivity and precision. For low risk cases the f1 score is near perfect, as expected with the extremely high precision and sensitivity rates of the model with regards to low risk cases.

## Conclusion

As the EEC model is the top performing model, it is the one I would recommend using if necessary. While the precision identifying high risk cases is extremely low at 0.07, the sensitivity of finding same is high at 0.91 and the overall balanced accuracy score of the model is good. Although this means many low risk cases will be mistakenly flagged as high risk, 91% of high risk cases would be identified as such. In this case, sensitivity is more important than precision as it is better to flag all high risk cases and more, than to provide too many loans to high risk cases. 

As a disclaimer, I do not believe this model is perfect and I still believe it should be improved upon. The closer the sensitivity for high risk cases can get to 1, or 100%, while maintaining performance elsewhere, the better.
