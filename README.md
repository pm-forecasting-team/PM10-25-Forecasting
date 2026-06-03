# Multi-Output Air Pollution Prediction

PM10(미세먼지)와 PM2.5(초미세먼지)를 동시에 예측하기 위한
Multi-Output Regression 기반 대기질 예측 프로젝트입니다.

## Project Overview

본 프로젝트는 경기도 지역의 대기오염 데이터를 활용하여

- PM10
- PM2.5

를 동시에 예측하는 머신러닝 모델을 구축하고,
다양한 회귀 모델의 성능을 비교하는 것을 목표로 합니다.

## Dataset

### Source

경기도 대기환경정보 공개 데이터

### Target Variables

- PM10
- PM2.5

### Features

- SO₂
- CO
- NO₂
- O₃
- 요일 정보
- 계절 정보
- Lag Features

## Data Preprocessing

- Missing Value Handling
- Feature Engineering
- Lag Feature Creation
- Train / Validation / Test Split

## Models

### Linear Regression

기준(Baseline) 모델로 사용

### Random Forest Regressor

비선형 관계 학습을 위한 앙상블 모델

### Extra Trees Regressor

강한 무작위성을 적용한 트리 기반 앙상블 모델

## Hyperparameter Optimization

Random Search 기반 최적화 수행

Example:

```python
{
    "n_estimators": [100, 300, 500],
    "max_depth": [None, 5, 10, 15],
    "min_samples_split": [2, 5, 10]
}
