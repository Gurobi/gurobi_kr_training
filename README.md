# Gurobi 한국 사용자 교육 자료

<p align="center">
  <img src="qrcode.png" alt="Repository QR Code" width="150"/>
</p>

이 저장소는 **Gurobi Optimizer**를 처음 접하는 한국 사용자를 위한 실습 중심 교육 자료를 제공합니다.
Python(`gurobipy`)을 사용하여 수리 최적화(Mathematical Optimization)의 기본 개념부터 배합 및 생산 계획 예제까지 단계적으로 학습할 수 있습니다.

---

## 목차

각 노트북은 **실습(실습)** 버전과 **정답(답안)** 버전으로 구성되어 있습니다.

| # | 주제 | 실습 | 답안 |
|---|------|------|------|
| 0 | Gurobi 기본 예제 (mip1.py) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/0_Gurobi%20%EA%B8%B0%EB%B3%B8%20%EC%98%88%EC%A0%9C%20(mip1.py).ipynb) | - |
| 1 | 이진 정수 계획법 (BIP) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/1_BIP_%EC%8B%A4%EC%8A%B5.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/1_BIP_%EB%8B%B5%EC%95%88.ipynb) |
| 2 | 주스 배합 문제 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/2_%EC%A3%BC%EC%8A%A4%EB%B0%B0%ED%95%A9%EB%AC%B8%EC%A0%9C_%EC%8B%A4%EC%8A%B5.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/2_%EC%A3%BC%EC%8A%A4%EB%B0%B0%ED%95%A9%EB%AC%B8%EC%A0%9C_%EB%8B%B5%EC%95%88.ipynb) |
| 3 | 생산 재고 관리 문제 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/3_%EC%83%9D%EC%82%B0%EC%9E%AC%EA%B3%A0%EA%B4%80%EB%A6%AC%EB%AC%B8%EC%A0%9C_%EC%8B%A4%EC%8A%B5.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/3_%EC%83%9D%EC%82%B0%EC%9E%AC%EA%B3%A0%EA%B4%80%EB%A6%AC%EB%AC%B8%EC%A0%9C_%EB%8B%B5%EC%95%88.ipynb) |

---

## 강의 내용

### 0. Gurobi 기본 예제 (mip1.py)
Gurobi 공식 문서의 첫 번째 예제를 통해 `gurobipy`의 기본 사용법을 익힙니다.

- 모델 생성, 변수 추가, 목적함수 및 제약 조건 설정
- `model.optimize()` 실행 및 결과 확인
- 참고: [Gurobi mip1 예제](https://docs.gurobi.com/projects/examples/en/current/examples/python/mip1.html)

### 1. 이진 정수 계획법 (Binary Integer Programming)
단순한 0-1 변수로 구성된 최적화 문제를 직접 모델링하고 풀어봅니다.

- 의사결정 변수, 목적함수, 제약 조건의 구조적 이해
- Gurobi 최적화 상태(Optimization Status) 해석
- 최적해 추출 및 분석

### 2. 주스 배합 문제 (Blending Problem)
여러 원재료를 혼합하여 제품을 생산하는 **배합 최적화** 문제를 다룹니다.

- 실제 생산 현장에서 발생하는 비율/비용 제약 모델링
- 선형 계획법(LP)을 활용한 원가 최소화
- 결과 시각화 및 분석

### 3. 생산 재고 관리 문제 (Production & Inventory Management)
다기간(Multi-period) 생산 계획 및 재고 관리 문제를 최적화합니다.

- 시간 인덱스를 활용한 동적 모델링
- 생산량, 재고량, 수요 충족을 동시에 고려하는 복합 제약 설계
- 비용 최소화 관점의 공급망 최적화

---

## 시작하기

### 방법 1: Google Colab (권장)
위 표의 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]() 버튼을 클릭하면 별도 설치 없이 브라우저에서 바로 실행할 수 있습니다.
각 노트북 상단에 `gurobipy` 설치 코드가 포함되어 있습니다.

> **참고**: Google Colab에서는 Gurobi의 무료 학술 라이선스(Academic License) 또는 제한된 크기의 문제를 풀 수 있는 무료 라이선스가 자동으로 적용됩니다.

### 방법 2: 로컬 환경
```bash
# 저장소 클론
git clone https://github.com/Gurobi/gurobi_kr_training.git
cd gurobi_kr_training

# gurobipy 설치
pip install gurobipy

# Jupyter 실행
jupyter notebook
```

로컬 실행을 위해서는 유효한 Gurobi 라이선스가 필요합니다.
학술 사용자는 [Gurobi Academic License](https://www.gurobi.com/academia/academic-program-and-licenses/)를 무료로 신청할 수 있습니다.

---

## 참고 자료

- [Gurobi 공식 문서](https://docs.gurobi.com/)
- [gurobipy API 레퍼런스](https://docs.gurobi.com/projects/optimizer/en/current/reference/python/)
- [Gurobi 예제 모음](https://docs.gurobi.com/projects/examples/en/current/)
