# Gurobi 한국 사용자 교육 자료

<p align="center">
  <img src="qrcode.png" alt="Repository QR Code" width="250"/>
</p>

이 저장소는 **Gurobi Optimizer**를 처음 접하는 한국 사용자를 위한 실습 중심 교육 자료를 제공합니다.
**초급** 과정에서는 Python(`gurobipy`)으로 수리 최적화(Mathematical Optimization)의 기본 개념부터
배합 및 생산 계획 예제까지 직접 코딩하며 익히고, **중급** 과정에서는 Gurobi의 AI 에이전트인
**Intelligence Hub**(Modeler, Explainer)를 활용해 모델을 만들고 진단하는 방법을 다룹니다.

---

## 목차

### 초급

각 노트북은 **실습** 버전과 **답안** 버전으로 구성되어 있습니다.

| # | 주제 | 실습 | 답안 |
|---|------|------|------|
| 0 | Gurobi 기본 예제 (mip1.py) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/%EC%B4%88%EA%B8%89/0_Gurobi%20%EA%B8%B0%EB%B3%B8%20%EC%98%88%EC%A0%9C%20(mip1.py).ipynb) | - |
| 1 | 이진 정수 계획법 (BIP) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/%EC%B4%88%EA%B8%89/1_BIP_%EC%8B%A4%EC%8A%B5.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/%EC%B4%88%EA%B8%89/1_BIP_%EB%8B%B5%EC%95%88.ipynb) |
| 2 | 주스 배합 문제 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/%EC%B4%88%EA%B8%89/2_%EC%A3%BC%EC%8A%A4%EB%B0%B0%ED%95%A9%EB%AC%B8%EC%A0%9C_%EC%8B%A4%EC%8A%B5.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/%EC%B4%88%EA%B8%89/2_%EC%A3%BC%EC%8A%A4%EB%B0%B0%ED%95%A9%EB%AC%B8%EC%A0%9C_%EB%8B%B5%EC%95%88.ipynb) |
| 3 | 생산 재고 관리 문제 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/%EC%B4%88%EA%B8%89/3_%EC%83%9D%EC%82%B0%EC%9E%AC%EA%B3%A0%EA%B4%80%EB%A6%AC%EB%AC%B8%EC%A0%9C_%EC%8B%A4%EC%8A%B5.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gurobi/gurobi_kr_training/blob/main/%EC%B4%88%EA%B8%89/3_%EC%83%9D%EC%82%B0%EC%9E%AC%EA%B3%A0%EA%B4%80%EB%A6%AC%EB%AC%B8%EC%A0%9C_%EB%8B%B5%EC%95%88.ipynb) |

### 중급

Gurobi **Intelligence Hub**([intelligence.gurobi.com](https://intelligence.gurobi.com))의 AI
에이전트를 사용하는 실습입니다. 실제 모델링·진단 작업은 웹 브라우저에서 진행하며, 이 문서들은
코드 없이 문제 설명·진행 가이드·예상 결과만 제공합니다 (실습/답안 구분 없음, Hub 로그인 계정 필요).

| # | 주제 | 문서 |
|---|------|------|
| 4 | Modeler로 모델 만들기 | [4_Modeler.md](중급/4_Modeler.md) |
| 5 | Explainer로 모델 진단하기 | [5_Explainer.md](중급/5_Explainer.md) |

`중급/3_생산재고관리문제_data.csv`는 4번 문서 워밍업(Part 0)에서, `중급/moodel.lp`와
`중급/moodel_repaired.lp`는 5번 문서 실습에서 각각 업로드하는 데이터/모델 파일입니다.

---

## 강의 내용

### 초급

#### 0. Gurobi 기본 예제 (mip1.py)
Gurobi 공식 문서의 첫 번째 예제를 통해 `gurobipy`의 기본 사용법을 익힙니다.

- 모델 생성, 변수 추가, 목적함수 및 제약 조건 설정
- `model.optimize()` 실행 및 결과 확인
- 참고: [Gurobi mip1 예제](https://docs.gurobi.com/projects/examples/en/current/examples/python/mip1.html)

#### 1. 이진 정수 계획법 (Binary Integer Programming)
단순한 0-1 변수로 구성된 최적화 문제를 직접 모델링하고 풀어봅니다.

- 의사결정 변수, 목적함수, 제약 조건의 구조적 이해
- Gurobi 최적화 상태(Optimization Status) 해석
- 최적해 추출 및 분석

#### 2. 주스 배합 문제 (Blending Problem)
여러 원재료를 혼합하여 제품을 생산하는 **배합 최적화** 문제를 다룹니다.

- 실제 생산 현장에서 발생하는 비율/비용 제약 모델링
- 선형 계획법(LP)을 활용한 원가 최소화
- 결과 시각화 및 분석

#### 3. 생산 재고 관리 문제 (Production & Inventory Management)
다기간(Multi-period) 생산 계획 및 재고 관리 문제를 최적화합니다.

- 시간 인덱스를 활용한 동적 모델링
- 생산량, 재고량, 수요 충족을 동시에 고려하는 복합 제약 설계
- 비용 최소화 관점의 공급망 최적화

### 중급

#### 4. Modeler로 모델 만들기 (`4_Modeler.md`)
자연어로 설명한 문제를 **Modeler**(Beta)가 스펙 → `gurobipy` 코드 → 테스트까지 만들어주는 과정을
경험합니다. 세 부분(Part 0~1, 부록)으로 구성됩니다.

- Part 0. 워밍업: 초급에서 직접 코딩했던 문제를 Modeler에 맡겨 결과를 비교 — AI가 만든 모델을 검증하는 습관
- Part 1. 본 실습: 프리미엄 유제품 음료 하나를 생산하는 단순화된 문제를 30분 안에 모델링해 feasible한
  최적해까지 완성
- 부록. 전체 공정 모델: 같은 공장을 원유 2종·제품 5종으로 확장한 버전 — 여기서 만든 모델이 5번
  문서에서 이어서 사용됩니다.

#### 5. Explainer로 모델 진단하기 (`5_Explainer.md`)
**Explainer**(Experimental)로 실행 불가능(infeasible)한 모델을 진단·복구·분석합니다.

- Infeasibility Diagnosis: IIS(충돌하는 최소 제약 집합)로 원인 진단
- Feasibility Restoration: `feasRelax`로 최소 완화량 계산
- Sensitivity Analysis: 섀도우 프라이스로 투자 우선순위 도출

---

## 시작하기

### 방법 1: Google Colab (권장)
위 표의 [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]() 버튼을 클릭하면 별도 설치 없이 브라우저에서 바로 실행할 수 있습니다.
초급 노트북 상단에는 `gurobipy` 설치 코드가 포함되어 있습니다.

> **참고**: Google Colab에서는 Gurobi의 무료 학술 라이선스(Academic License) 또는 제한된 크기의 문제를 풀 수 있는 무료 라이선스가 자동으로 적용됩니다.

중급 문서(4, 5번)는 `.md` 가이드 문서로, 코드 실행 없이 [intelligence.gurobi.com](https://intelligence.gurobi.com)
에서 진행합니다. Intelligence Hub 로그인 계정이 필요합니다.

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

## 마무리

- **초급** 과정에서는 문제를 직접 수식으로 세우고 `gurobipy` 코드를 한 줄씩 작성했습니다.
- **중급** 과정에서는 **Modeler**로 자연어에서 검증된 모델을 얻고, **Explainer**로 그 모델을
  진단·복구·분석하는 과정을 경험합니다.

실제 현업에서는 이 두 에이전트를 조합해 "모델링 → 운영 중 이슈 대응"까지 이어지는 워크플로를
구성할 수 있습니다. 다만 두 과정 모두에서 강조하듯, AI 에이전트가 만든 모델과 설명을 무조건
신뢰하지 말고 acceptance test와 같은 방법으로 직접 검증하는 습관을 들이는 것이 중요합니다.

---

## 참고 자료

- [Gurobi 공식 문서](https://docs.gurobi.com/)
- [gurobipy API 레퍼런스](https://docs.gurobi.com/projects/optimizer/en/current/reference/python/)
- [Gurobi 예제 모음](https://docs.gurobi.com/projects/examples/en/current/)
- [Gurobi Intelligence Hub](https://intelligence.gurobi.com)
