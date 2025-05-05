# AB Test Using Gaming Data

이 프로젝트는 **게임 내 A/B 테스트 데이터를 활용하여 사용자 행동 및 수익성을 비교 평가**하는 Python 기반 분석 노트북입니다.  
`pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy` 등 Python 데이터 분석 라이브러리를 활용하여 **Engagement Score**와 **Monetization Score**를 산출하고 두 집단 간의 차이를 시각화합니다.

---

## 📦 **프로젝트 구조**
- `AB_test_using_gaming_data.ipynb`  
  → 본 프로젝트의 메인 분석 노트북입니다.

- `Control_Group_Data.csv`, `Test_Group_Data.csv`  
  → A/B 테스트의 Control 그룹과 Test 그룹 데이터 (로컬 경로로 불러오기)

---

## 📝 **주요 작업 내용**

1. **데이터 로드**
   - `Control_Group_Data.csv`, `Test_Group_Data.csv`를 pandas DataFrame으로 로드
   - 각 그룹의 기본 통계 및 데이터 미리보기
  
2. **기본 분석**
   - 성별(Gender)별 `Average_Purchase_Value` 평균 비교
   - 데이터의 기본 분포 확인

3. **파생 지표 계산**
   - **Engagement Score**:  
     `Sessions`, `Time_Spent_Minutes`, `Actions_Per_Session`의 평균으로 계산
   - **Monetization Score**:  
     `Purchases`와 `Average_Purchase_Value`를 곱해 10으로 나누어 계산
   - 두 점수를 각 그룹에 새 변수로 추가

4. **데이터 통합**
   - Control, Test 그룹 데이터를 하나의 DataFrame으로 결합

5. **시각화 및 통계분석**
   - 두 그룹 간 `Engagement Score` 및 `Monetization Score` 분포 시각화
   - `scipy.stats`를 사용한 통계적 유의성 검정 (z-test 등)

---

## 📊 **결과 해석**
- **성별에 따른 구매 가치 차이는 크지 않음**
- Test 그룹의 `Engagement Score`와 `Monetization Score`는 Control 그룹과의 비교를 통해 **테스트 효과(효과 존재 여부)**를 평가

---

## 💻 **사용 방법**
1. `AB_test_using_gaming_data.ipynb`를 Jupyter Notebook 또는 Google Colab에서 실행
2. 데이터 파일 경로를 본인의 로컬 경로로 수정 (예: Windows 경로 → 상대경로/절대경로 변경)
3. 각 코드 셀을 순차적으로 실행

---

## 🧩 **필요한 라이브러리**
- pandas
- numpy
- scipy
- matplotlib
- seaborn

## 🔗 참고 자료

- [Optimizing Game Design with Data: My Journey in A/B Testing for Engagement and Monetization](https://halbeeb.medium.com/optimizing-game-design-with-data-my-journey-in-a-b-testing-for-engagement-and-monetization-d812bf58360f)
- [Practical Statistics for Data Scientists](https://www.oreilly.com/library/view/practical-statistics-for/9781491952955/)

