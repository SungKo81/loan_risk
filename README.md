### 대출 위험도 예측 모델
- SKN 머신러닝 수업 진행과제
- cs_data.csv 파일을 기반으로 예측모델 생성
- 목표 : 테스트 기준 ROC_AUC_SCORE 0.85이상

사용 모듈
- pandas
- numpy
- scikit learn

진행순서
- pandas로 데이터를 불러온후, info() 를 사용하여 null 값 확인
- 데이터 전처리를 3가지 방법으로 진행.
    1. null값 삭제.
    2. income 은 평균. dependents는 중간값으로 변경.
    3. 그리디 서치를 사용
- 모델 예측 : RandomForestClassifier를 사용
- 평가 : ROC_AUC_SCORE 및 feature_importances 확인

결과
- null 값 삭제시 0.83으로 목표치에 미달
- 평균과 중간값으로 대체하여 진행시 0.84로 목표치 미달
- 그리디 서치 사용시 0.863으로 목표치 도달

결론
- 다소 시간이 걸릴지라도 다양한 파라미터값을 적용하여 최적의 모델을 찾을 필요가 있음.
- RandomForest만 사용하였지만, 다른 모델도 추가로 사용하여 개선된 모델을 찾을수 있을것으로 예상.
  
