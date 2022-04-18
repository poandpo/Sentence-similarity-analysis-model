## 한국어 문장의 유사도 분석 모델 프로젝트
두 문장의 의미적 유사도를 출력하는 모델 생성 및 학습하여 서비스화하는 프로젝트

### 데이터
두개의 문장들과 labels로 이루어진 데이터셋
(기업에서 제공한 데이터이기에 구체적인 정보를 비공개입니다.)

### 내용
- roberta-base tokenizer로 토큰화하고 전처리
- huggingface에서 가져온 klue/roberta pre-trained model로 fine tuning
- batch size, learning_rate,epoch, weight_decay 중점으로 하이퍼파라미터 튜닝
- 두 문장의 문장 유사도 값을 추출하는 모델 만듦
- f1는 0.87, pearson’r는 0.88 성능까지 도달
- 해당 모델을  Flask로 API 구축

### 한계 및 보완점
- 데이터 EDA를 진행하지 않았기에 이를 수행하여 EDA를 통해 더 다양한 가설 수립하기
- 해당 모델은 f1 중심으로 하이퍼파라미터 튜닝을 했기에 pearson’r 를 다 같이 고려할 수 있는 방법으로 실행해보기
___

