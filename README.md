# Python
이상 신용거래 예측 데이터분석 대회에 나가는 스터디입니다. 2022-06-27 ~


## 스터디 방식
- ⏰ 스터디 시간 : 매주 수,금 오후 2시
- 📗 스터디 자료 : [데이콘 이상 신용거래 예측](https://dacon.io/competitions/official/235930/overview/description), [숫자 3D 이미지 분류 AI 경진대회](https://dacon.io/competitions/official/235951/overview/description)
  - 우수 코드를 분석하며 노트(Jupyter notebook)에 정리
  - 제안, 질문은 [Issues](https://github.com/deep-dive-in-python/main/issues) 를 이용
  
## 스터디 자료
- Anomaly Detection
  - [Anomaly Detection:소개 및 주요 문제와 핵심 용어, 산업 현장 적용 사례 정리](https://hoya012.github.io/blog/anomaly-detection-overview-1/)
  - [ANOMALY DETECTION 블로그](https://www.cognex.com/ko-kr/blogs/deep-learning/research/anomaly-detection-overview-1-introduction-anomaly-detection)
- 비지도 학습
  - [GAN 한시간만에 완전정복](https://www.youtube.com/watch?v=odpjk7_tGY0&t=69s)
  - [Semi-supervised learning 자료](https://blog.est.ai/2020/11/ssl/)
  - [unsupervised anomaly detection](https://www.kaggle.com/code/victorambonati/unsupervised-anomaly-detection) > 시계열 자료라 우리 분석과는 안맞는 점이 많음.
- XBOS
  - [XBOS한글해석자료](https://blog.naver.com/qkrdnjsrl0628/222802847577) : XBOS, based on K-MEAS clustering 
  - XBOS는 k-means clustering을 첫 번째로 사용하며, 그 이후, 교차 상호작용을 활용합니다.
  - 교차 상호작용(Cross interaction)을 사용함으로서, 최소의 클러스는 근처의 클러스터에 속하게 되므로, 변칙적인 문제가 발생하지 않습니다.
  - [XBOS영어해석자료](https://kanatoko.wordpress.com/2018/03/06/xbos-anomaly-detection/)
  - [XBOS깃허브코드](https://github.com/Kanatoko/XBOS-anomaly-detection)
- Pycaret
  - [pycaret:anomaly detection](https://insaid.medium.com/anomaly-detection-using-pycaret-38b267ed638b)
-----
- CNN MNIST 2d 분류 자료
  - [MNIST 99% with CNN 영상강의](https://www.youtube.com/watch?v=pQ9Y9ZagZBk&list=PLlMkM4tgfjnLSOjrEJN31gZATbcj_MpUm&index=40)
  - [영상강의의 코드 정리된 깃허브](https://github.com/hunkim/DeepLearningZeroToAll)


### 간편 Git 사용 방법
  - Git clone
```
https://github.com/deep-dive-in-python/main.git
```
  - Git 다운받기
```
git pull
```
  - Git 올리기
```
git add .
git commit -am "message"
git push 
```


## 스터디 기록
### 이상 신용거래 탐지- Unsupervised learning
- 2022-06-28-화 오전 10시
  - 스터디 계획 수립
  
- 2022-07-06-수 오전 10시
  - 발표: 연호(개요, k-평균 클러스터링), 승우(계층 클러스터링), 경선(DBSCAN,가우시안 혼합 모형)

- 2022-07-08-금 오전 10시
  - 발표: 연호(딥러닝 기초), 경선(CNN,RNN), 승우(AutoEncoder,GAN)

- 2022-07-13-수 오후 2시
  - [캐글 코드](https://www.kaggle.com/code/shivamb/semi-supervised-classification-using-autoencoders)
  
- 2022-07-15-금 오전 10시
  - [데이콘 코드 공유](https://dacon.io/competitions/official/235930/codeshare/5508?page=1&dtype=recent)
  - tsne를 이용한 시각화, 코드 공유 구현, encoder decoder 차원 축소>확대, 확대>축소 둘 다 해오기, 새로운 방법  
  - [unsupervised anomaly detection](https://www.kaggle.com/code/victorambonati/unsupervised-anomaly-detection)

- 2022-07-18-월 오전 10시
  - validation set의 feature별 class=1의 분포 표현
  - 사기거래가 0.1%이므로 semi-supervised 방법론을 이용해도 될 것 같다. 
  - 연호(XBOS), 승우(변수선택해서 AE 돌려오기), 경선([pycaret](https://towardsdatascience.com/unsupervised-anomaly-detection-in-python-f2e61be17c2b))
  - 목표: 정확도 퍼센트 가져오기

- 2022-07-21-목 오전 10시
  - 정확도 비교 및 모델 선정
  - 승우: 이상치 over sampling 정상거래는 under sampling & Feature engineering
  - 연호: ANOGAN으로 구현
  - 경선: AE 스스로 짜오기
  - 파일 하나씩 제출해서 다음 스터디때 팀 만들 수 있게 하기

- 2022-07-25-월 오전 10시
  - data 분석, 모델 평가, 분석 등
  - over sampling, under sampling은 labeled 데이터가 아니라서 의미가 없을듯.
  - train class에서 validation의 thr 조정을 어떻게 해야할지 모름.
  - ANOGAN과 VAE를 시도하였으나 labeled가 아니라서 고전중.
  - feature를 forward selection 하려고 했으나 아직 진행중.
  - feature의 selection을 어떤 기준으로 cutoff할지 이론적인 비모수 방법론 이용.


  - 다음 시간에 할 것: cutoff 방법론 적용, forward selection 다음 시간에 제출.
  - 경선: 지금까지 한거 정리해서 글쓰기.
  - 연호: 다음 대회 찾아오기

- 2022-07-28-목 오전 11시
  > 데이터 경진대회(연호)
    1. [3d 이미지](https://dacon.io/competitions/official/235951/data) : 숫자 3D 이미지 분류 AI 모델 개발
    2. [한강 수위예측](https://dacon.io/competitions/official/235949/overview/description) : 시계열
    3. [American Express](https://www.kaggle.com/competitions/amex-default-prediction/overview)
    4. cos pro 자격증 by studying at the site of 백준(https://www.acmicpc.net/)
  > 승우, 변수선택 코드 설명(완료)
  > 경선, 취침후 사망
-----
### 숫자 3d 이미지 분류 AI모델 개발-computer vision  
- 2022-08-05-금 오후 2시
  - 경선: 코드 정리 설명
  - 다음 스터디 주제로 [숫자 3D 이미지 분류 AI 모델 개발](https://dacon.io/competitions/official/235951/data) 선정
  
- 2022-08-09-화 오후 2시
  - 스터디 자료 링크를 활용하여 2d MNIST 이미지 분류 코드 짜오기.
  - 영상강의로 CNN 공부해오기.
