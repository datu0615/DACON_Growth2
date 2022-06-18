# DACON_Growth2
![v2](https://user-images.githubusercontent.com/84311270/174434235-a5149804-4091-4d9e-808f-49c86fa7bbac.png)

Algorithm] 청경채 사진과 환경 데이터를 활용한 잎면적 예측 알고리즘 개발
[Analytics] 적상추 데이터 활용 생육정도를 알 수 있는 정량 지표 발굴

## Dataset  
 train [Folder] : 학습용 청경채 데이터셋 (1592장)  
	│	├ CASE01 : 각 케이스 별 데이터  
	│	│	├ image : 이미지 데이터  
	│	│	├ meta : 환경 데이터  
	│	│		└ 촬영 된 시각으로부터 1일간 1분 간격으로 측정된 환경정보 데이터  
	│	│	└ label.csv :  
	│	│		└ img_name : 해당 이미지 파일명  
	│	│		└ leaf_weight : 해당 이미지가 촬영된 시점으로부터 1일 후의 잎 면적 (중량)  
	│	│  
	│	├ CASE02  
	│	├ CASE03  
	│	└ ...  

 test [Folder] : 테스트용 청경채 데이터셋 (460장)  
	│	├ image : 이미지 데이터  
	│	├ meta : 환경 데이터  
	│		└ 촬영 된 시각으로부터 1일간 1분 간격으로 측정된 환경정보 데이터  
	│

sample_submission.csv  
	└ img_name : 해당 이미지 파일명  
	└ leaf_weight : 해당 이미지가 촬영된 시점으로부터 1일 후의 잎 면적 (중량)  
  
  ## Model
   plantcv 모듈을 이용하여 청경채 사진 마스킹 및 배경 제거, 그리고 convenxt-large 모델을 사용하여 
