# recommendation-itemKNN
implementation of item based collaborative filtering


# ■ Issue

## - Abook의 경우 

## - Last-FM 데이터셋 활용시 memory error
item KNN에 Last-FM 데이터셋 적용시 너무 큰 Matrix가 생성되어 오류

-> Dataframe sim 계산까지는 
-> 로컬 메모리 32G 기준으로 8000명씩 잘라서 matrix 생성 및 평가


# ■ 데이터셋 Description & Reference

|Dataset|Users|Items|Inter|
|:---:|:---:|:---:|:---:|
|ML-small||||
|ML-1m|6,040|3,706|1,000,209|
|Last-FM|23,566|48,123|3,034,796|
|Amazon-Book|70,679|24,915|847,733|


## - Movie-Lens small

출처 : https://www.kaggle.com/rounakbanik/the-movies-dataset

## - Movie-Lens 1M

출처 : https://grouplens.org/datasets/movielens/1m/

## - Amazon-Book & Last-FM

출처 : https://github.com/xiangwang1223/knowledge_graph_attention_network
