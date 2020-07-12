# Dimensionality Reduction Overview

> A comparison between Statistical, Machine Learning, PCA, SVD, and REF methods


## Conclusion 

### Data
KDD'99 an Intrusion Detection Dataset
* [Very Detailed Analysis](https://www.ee.ryerson.ca/~bagheri/papers/cisda.pdf)
### Benchmark
```
eclf = VotingClassifier(estimators=[('DecisionTreeClassifier', DTC), ('RandomForestClassifier', RFC),('ExtraTreesClassifier',ETC)], voting='hard')
_ = eclf.fit(X_train, y_train)
pred = eclf.score(X_test,y_test)
print("Acc: %0.10f" % (pred))
```

### Overview of methods
* Removing the features with the _lowest correlation_ and the lowest _standard deviation_   
* `.feature_importances_` from sklearn.ensemble.{x,y,z} 
* Recursive Feature Elimination
* Principal Component Analysis
* Singular Value Decomposition





### Results 

#### RFE; 6 features
* Acc: 0.9798537512

#### PCA; 6 features
* Acc: 0.9737667829

#### TruncatedSVD; 6 features
* Acc: 0.9765543989
  * if dims = 2, Acc: 0.9441938134

#### Feature Elimination(statistical) + "extream" feature Elimination(ML); 6 features
* Acc: 0.9619160483  

#### Feature Elimination(statistical) + extra feature Elimination(ML); 11 features
* Acc: 0.9832743041  

#### Feature Elimination(statistical) + feature Elimination(ML); 18 features
* Acc: 0.9865467229 

#### Feature Elimination(statistical); 27 features
* Acc: 0.9890784707 

#### From all data; 41 features
* Acc: 0.9935763632
