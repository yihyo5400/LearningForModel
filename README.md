# LearningForModel

1. xgboost는 설치를 해야지 쓸 수 있다.. 
  anaconda로 jupyter notebook을 이용하므로 pip install-이 아닌 conda install -c conda-forge xgboost 를 통해 설치했어야 함
    https://bobbyhadz.com/blog/python-no-module-named-xgboost
    
2. 예측과 분류에 대한 이해 부족으로 연속형 종속변수를 갖는 데이터에 RandomForestClassifier을 쓰고 있었음. 예측은 RandomForestRegressor임
   또한 svm에서 svc만 써봐서 svr이 있는지 몰랐음. 더 공부해야 함
   
3. rmse로 예측모델을 평가했는데, 어떤건 몇십만이나오고 어떤건 0.000003이 나왔다.. 
    이유를 살펴보니 train model에 종속변수를 포함하고 있었다.
    train_test_split로 valid data를 분류한 뒤에 drop을 해주자.
    
4. rmsle와 rmse는 다른걸로 알고있는데 찾아본 블로그에서는 둘 다 똑같은 식을 쓰고 있다..? 자동으로 로그를 씌워주나?..
    https://www.kaggle.com/code/blighpark/t2-4-house-prices-regression  rmsle를 쓰는데 식을 보면 rmse다.
    https://growingsaja.tistory.com/233
    첫번째 링크가 틀린 듯..
    
5. 예측 문제에 roc-auc를 적용하려고 하니까 안먹었다. 당연함. 이진분류를 위한 지표임
    친절하게 ValueError: continuous format is not supported 라고 오류코드가 나와줘서 금방 해결했다.
