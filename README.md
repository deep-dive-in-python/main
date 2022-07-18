# Python
이상 신용거래 예측 데이터분석 대회에 나가는 스터디입니다. 2022-06-27 ~


## 스터디 방식
- ⏰ 스터디 시간 : 매주 수,금 10시
- 📗 스터디 자료 : [데이콘 이상 신용거래 예측](https://dacon.io/competitions/official/235930/overview/description)
  - 우수 코드를 분석하며 노트(Jupyter notebook)에 정리
  - 제안, 질문은 [Issues](https://github.com/deep-dive-in-python/main/issues) 를 이용
  
## 스터디 자료
- Anomaly Detection
  - [Anomaly Detection:소개 및 주요 문제와 핵심 용어, 산업 현장 적용 사례 정리](https://hoya012.github.io/blog/anomaly-detection-overview-1/)
  - [ANOMALY DETECTION 블로그](https://www.cognex.com/ko-kr/blogs/deep-learning/research/anomaly-detection-overview-1-introduction-anomaly-detection)
-----
- 비지도 학습
  - [GAN 한시간만에 완전정복](https://www.youtube.com/watch?v=odpjk7_tGY0&t=69s)
  - [Semi-supervised learning 자료](https://blog.est.ai/2020/11/ssl/)
  - [unsupervised anomaly detection](https://www.kaggle.com/code/victorambonati/unsupervised-anomaly-detection) > 시계열 자료라 우리 분석과는 안맞는 점이 많음.
-----
- XBOS
  - [XBOS한글해석자료](https://blog.naver.com/qkrdnjsrl0628/222802847577) : XBOS, based on K-MEAS clustering 
  - XBOS는 k-means clustering을 첫 번째로 사용하며, 그 이후, 교차 상호작용을 활용합니다.
  - 교차 상호작용(Cross interaction)을 사용함으로서, 최소의 클러스는 근처의 클러스터에 속하게 되므로, 변칙적인 문제가 발생하지 않습니다.
  - [XBOS영어해석자료](https://kanatoko.wordpress.com/2018/03/06/xbos-anomaly-detection/)
  - [XBOS깃허브코드](https://github.com/Kanatoko/XBOS-anomaly-detection)
-----
- Pycaret
  - [pycaret:anomaly detection](https://insaid.medium.com/anomaly-detection-using-pycaret-38b267ed638b)


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

- 2022-07-25-월 오전 10시
  - data 분석, 모델 평가, 분석 등
