# recommendation-itemKNN
implementation of item based collaborative filtering

# Issue

## Last-FM 데이터셋 활용시 memory error
item KNN에 Last-FM 데이터셋 적용시 너무 큰 Matrix가 생성되어 오류

-> Dataframe sim 계산까지는 
-> 로컬 메모리 32G 기준으로 8000명씩 잘라서 matrix 생성 및 평가
