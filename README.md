# recommendation-itemKNN
implementation of item based collaborative filtering

# ■ 데이터셋 Description

|Dataset|#Users|#Items|#Interactions|
|:---:|:---:|:---:|:---:|
|ML-small||||
|ML-1m|6,040|3,706|1,000,209|
|Last-FM|23,566|48,123|3,034,796|
|Amazon-Book|70,679|24,915|847,733|

-> 데이터셋은 Knoledge Graph 관련 실험을 위해 metadata, triple이 존재하는 것 기준으로 사용

# ■ Evaluation Results

## - item POP & item KNN
### [Movie Lens - small]

|Model|HR@5|HR@10|HR@20|NDCG@5|NDCG@10|NDCG@20|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|itemPOP|0.188|0.292|0.408|0.122|0.1575|0.186|
|itemKNN|0.304|0.405|0.518|0.230|0.263|0.290|

### [Movie Lens - 1M]

|Model|HR@5|HR@10|HR@20|NDCG@5|NDCG@10|NDCG@20|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|itemPOP|0.311|0.455|0.638|0.208|0.255|0.301|
|itemKNN|0.368|0.521|0.707|0.255|0.306|0.351|


### [Last - FM]

|Model|HR@5|HR@10|HR@20|NDCG@5|NDCG@10|NDCG@20|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|itemPOP|0.344|0.470|0.621|0.242|0.284|0.322|
|itemKNN|||||||

## - BPR

### emb size experiment, K=10

![image](https://user-images.githubusercontent.com/67678405/118928824-b3e3ca00-b97e-11eb-8173-23e873c7993f.png)
![image](https://user-images.githubusercontent.com/67678405/118928758-9f9fcd00-b97e-11eb-8ec6-04f1d96ac56c.png)
![image](https://user-images.githubusercontent.com/67678405/118928767-a3335400-b97e-11eb-98d7-199a44a3d7e2.png)


### K size experiment, emb size=16

# ■ Issue

## - Abook은 Time, Computing 문제로 추후 진행 예정

## - Last-FM 데이터셋 활용시 memory error
item KNN에 Last-FM 데이터셋 적용시 너무 큰 Matrix가 생성되어 오류

-> Dataframe sim 계산까지는 
-> 로컬 메모리 32G 기준으로 8000명씩 잘라서 matrix 생성 및 평가


# ■ 데이터셋 Reference

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
