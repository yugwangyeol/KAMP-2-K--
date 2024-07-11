# KAMP : 2022년 제2회 K-인공지능 제조데이터 분석 경진대회
시계열 분석 기반 용해물 품질 예측AI 모델개발

<br/>

## 1. 배경 & 목적
 
- KAMP(인공지능 중소벤처 제조플랫폼) 내 등재된 제조 AI 데이터 셋을 활용하여 중소 기업이 직면할 수 있는 공통문제를 해결 또는 개선할 수 있는 우수한 인공지능 분석모델 개발

<br/>

## 2. 주최/주관 & 성과

- 주최/주관: KAIST, KOSMO(스마트제조혁신추진단), 중소벤처기업부
- 참가 대상: 만 19세 이상의 제조 AI데이터셋을 활용한 인공지능 분석에 관심 있는 누구나
- 성과 : 2022년 제2회 K-인공지능 제조데이터 분석 경진대회 최우수상 (2등)

<br/>

![KakaoTalk_20221207_091355702](https://github.com/yugwangyeol/KAMP/assets/72298825/a5663620-0bc8-4ff1-b7a2-edbbc6121d65)


<br/>

## 3. 프로젝트 기간

- 프로젝트 시간: 2022년 10월 26일
- 제출마감: 2022년 11월 9일
- 1차 서류 심사 결과: 2022년 11월 18일
- PT 발표 심사 : 2022년 11월 30일
- 시상식 : 2022년 12월 06일

<br/>

## 4. 프로젝트 소개

&nbsp;&nbsp;&nbsp;&nbsp; 용해 공정은 원재료의 전처리를 수행하는 첫 번째 단계로 공정의 품질이 후고정 및 완제품의 품지에 미치는 영향이 큼, 용해 품질에 영향을 미치는 많은 요인들이 존재하며, 현장 작업자는 경험과 노하우에 의존, 중간에 내용물을 확인하는 것이 불가능 하여 생산 단계가 상당히 많이 진행되기까지 품질이 보장되지 못함
<br/>
&nbsp;&nbsp;&nbsp;&nbsp; 이를 해결하기 위해 공정 중 실시간으로 변화하는 설비 운영값과 주요 품질검사항목의 결과값을 모델링하고, 생산 품질 예측 및 공정 제어간 필요 요소 분석을 진행함
<br/>
![스크린샷 2024-07-10 192925](https://github.com/yugwangyeol/KAMP/assets/72298825/eefae2c3-f680-49c9-8fa3-b85dfa915684)
<br/>
&nbsp;&nbsp;&nbsp;&nbsp; 위와 같은 시각화를 통해 가정을 세움, 용해 온도 및 교반 속도의 주기는 1분을 기준으로 증가 및 반복, 품질이 불량일 때, 온돈 &교반 속도가 증가 후 감소할 떄 순간적으로 정상에서 불량으로 변하는 현상등의 가정을 세움
<br/>
![스크린샷 2024-07-10 193229](https://github.com/yugwangyeol/KAMP/assets/72298825/a439106a-0a20-4d45-93b5-54c16a4f4d78)
<br/>
&nbsp;&nbsp;&nbsp;&nbsp; 총 3단계를 걸쳐 최종 모델을 선정,  Task가 이상탐지를 목표로 하므로 이상 탐지 모델들을 사용, 그러나 데이터의 분포와 특징이 이상치를 이루고 있지 않아 성능이 낮았음. 이후 데이터를 전처리 하여 ML 진행했으나 성능이 좋지 않아 딥러닝 모델 사용. LSTM과 CNN_LSTM을 사용하여 이상치 탐지 진행. 좋은 성능을 보인 CNN_LSTM을 최종 모델로 사용
&nbsp;&nbsp;&nbsp;&nbsp; 최종 모델을 바탕으로 SHAP을 활용하여, 공정 제어에 중요한 요소와 요소의 영향력을 파악함. 이를 바탕으로 기계 이상치까지 제시함

## 5. Process

### ch.1 Data EDA & Preprocessing

- EDA
- Preprocessing

---

### ch.2 Modeling  

- KeyPoint Detection (YoloV8, RPM Pose)
- Object Tracking (CoTracker, Pips)
- STT (SeamlessM$T, Whisper)

---

### ch.3 Post-processing

- 이상치 탐지 모델(isolationforest,Elliptic Envelope)
- ML (Pycaret,Catboost)
- DL (LSTM,CNN_LSTM)

---

### ch.4 결과 분석

- SHAP
- 분석


<br/>

## 6. 프로젝트 팀원 및 담당 역할

**[팀원]**

- 학부생 3명

**[담당 역할]**

- 기획
- 데이터 전처리
- 모델링

<br/>

## 7. 발표 자료&참고 자료

[2022 KAMP 발표 자료](https://github.com/yugwangyeol/KAMP/blob/main/%EB%B0%9C%ED%91%9C%EC%9E%90%EB%A3%8C_%EC%A0%9C%EC%9D%BC_%EC%B5%9C%EC%A2%85%EB%B3%B8.pdf)  

