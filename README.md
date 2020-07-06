# BankDepositPredict
The data shows the effects of direct marketing campaigns by a Portuguese banking institution
This model predicts whether a person with certain attributes has subscribed to the term deposit.

## Requirements
- Python 3.7
- Numpy
- Pandas
- Tensorflow

## How To
1 Download **bank-additional.csv**

2 Select attributes
    
    x = data.iloc[:, 0:10].values
    y = data.iloc[:, -1].values


3 Encode classes

    le = LabelEncoder()
    x[:, 1] = le.fit_transform(x[:, 1])
    x[:, 2] = le.fit_transform(x[:, 2])
    x[:, 3] = le.fit_transform(x[:, 3])
    x[:, 4] = le.fit_transform(x[:, 4])
    x[:, 5] = le.fit_transform(x[:, 5])
    x[:, 6] = le.fit_transform(x[:, 6])
    x[:, 7] = le.fit_transform(x[:, 7])
    x[:, 8] = le.fit_transform(x[:, 8])
    x[:, 9] = le.fit_transform(x[:, 9])
    y[:] = le.fit_transform(y[:])
   
 
4 Make into array

     x = np.array(x)
     y = np.array(y)
    

   

## Result
Print out the prediction result.

    predictions = model.predict(testData)
    print('Pass Prediction:')

If average score is 1, then pass. Else, non-pass.

    results = predictions.collect()
    for result in results:
        if result == 0:
            print("Non-pass")
        elif result == 1:
            print("Pass!")
            
## Acknowledgement

http://roycekimmons.com/tools/generated_data/exams

## Author
SeoHyun Kwon / @kwonddeoyeyo

## Team


