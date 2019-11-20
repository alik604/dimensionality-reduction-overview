# Dimensionality Reduction Overview

> A comparison between Statistical, Machine Learning, PCA, SVD, and REF methods


## Conclusion 

### Data
KDD'99 an Intrusion Detection Dataset
* [Vary Detailed Analysis](https://www.ee.ryerson.ca/~bagheri/papers/cisda.pdf)
### Benchmark
```
eclf = VotingClassifier(estimators=[('DecisionTreeClassifier', DTC), ('RandomForestClassifier', RFC),('ExtraTreesClassifier',ETC)], voting='hard')
_ = eclf.fit(X_train, y_train)
pred = eclf.score(X_test,y_test)
print("Acc: %0.10f" % (pred))
```

### overview of methords
* statistical 
* ipsum...
* lodri

#### RFE; 6
* Acc: 0.9798537512

#### PCA; 6
* Acc: 0.9737667829

#### TruncatedSVD; 6
* Acc: 0.9765543989
  * if dims = 2, Acc: 0.9441938134

#### Feature Elimination(statistical) + extra feature Elimination(ML); 6 features
* Acc: 0.9619160483  

#### Feature Elimination(statistical) + extra feature Elimination(ML); 11 features
* Acc: 0.9832743041  

#### Feature Elimination(statistical) + feature Elimination(ML); 18 features
* Acc: 0.9865467229 

#### Feature Elimination(statistical); 27 features
* Acc: 0.9890784707 

#### from all data; 41 features
* Acc: 0.9935763632
