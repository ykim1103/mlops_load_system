# mlops_loan_system (대출 시스템 구현)

![시스템구성](https://github.com/user-attachments/assets/df75bd21-05f1-47e8-addf-d32dae9ee6c1)

###### 1. 고객은 대출 신청 페이지에 접속하여 자신의 정보를 입력한다.
###### 2. 해당 정보들은 진진뱅크의 채널 시스템으로 전송된다.
###### 3. 채널 시스템은 고객들이 입력한 정보를 받아 그 정보를 바탕으로 대출평가 시스템에 신청자의 평가를 요청한다.
###### 4. 대출평가 시스템은 고객의 신용과 금융 상태를 분석하여 스코어 값을 채널 시스템에 전송한다. 
###### 5. 채널 시스템은 이 정보를 받아 진진뱅크 앱을 통해 고객에서 대출가능 여부를 전달한다. 

---------------------------------------------------------------------------------------------

## 대출적격 여부 예측 모델
- 고객이 대출을 실행하고 3개월 내에 부실이 발생할 것인지 여부를 예측하고 이를 기반으로 대출적격 여부 판단
- 일별로 신용대출 부적격에 대한 예측 스코어를 산출
- 매일 새벽 정해진 시각에 실행되는 배치 ML파이프라인을 개발하여 모델 예측결과 저장
- 대출 적격예측값(0:적격, 1:부적격)과 확률값을 조회하여 신용대출 적격여부 결과를 서비스에 제공

---------------------------------------------------------------------------------------------
## 데이터 정의
#### 원천 데이터
![데이터정의서](https://github.com/user-attachments/assets/91fd25ed-7569-40dc-8fc5-fb006f4a4bab)

#### 가공 후 학습에 활용할 최종 데이터셋 구성
![가공데이터](https://github.com/user-attachments/assets/0661487f-d0f1-45e5-8821-903b669d2645)
