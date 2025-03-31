# CRISIL_assignment
# Aim to predict company rating


## Data set analysis:

Data set contains numerical as well as categorical features ( encoded categorical features for further use)
Data set has text data, can be used for model building using NLP techniques.
Additionaly created sentimen score by using text data and used as feature in structured data.
Additionaly we can extract keywords to use them as features.
Assuming target column is multiclass type, i.e (column name : Rating)

## Models to build :
- model 1 : by using structured data( with added sentiment score featuer)
- model 2 : by using NLP technique (text data present in string_type)
- model 3 : by using combined structured data with text data sentiment score and extacted keywords from text data.


## Work flow

1- EDA and data cleaning :
    load data, check missing values,text data cleaning, lebelencoding and encoding

2- NLP text data handling :
    Clean text data, 
    Extract important keywords using Key-BERT model.
    create features of text data by using TF-IDF technique to use them as features.
    sentiment analysis to use sentiment score as feature by using roberta-base-sentiment model.

3- corelation :
    Top POSITIVE --
    ustret30ind       0.351786
    de_ratio          0.270509
    SPIndsprtrn       0.243338
    usind2CRSPMIV1    0.237503

    Bottom NEGATIVE --  
    debt_at          -0.181111
    monthCAP8RET     -0.198357
    pe_exi           -0.211383
    ustreb1ind       -0.218684
    monthusdcnt      -0.222704

4- Models used :
    Target is classification type problem need to use classification mode
    Target column  is "rating"
    Decision Tree

5- conclusion :
    Decision Tree model performed little better.
    sentiment score corelation : -0.042 (weak corelation, does nor significantly affect as its only 4%)

    model 1 accuracy : 10%
    model 2 accuracy : 05%
    model 3 accuracy : 20%

    Data corelation is weak to predict target.
    we can see that combined data with structured with text data with sentiment score improves model accuracy. (i.e Model 3 )
    Text data is not giving good result as its not sufficient.
