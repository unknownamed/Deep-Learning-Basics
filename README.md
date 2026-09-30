# Machine Learning Notes & Pest Classification Study

**머신러닝 기초 학습 기록과 해충 이미지 분류 주제의 PBL 자료를 정리한 저장소입니다.**

지도·비지도 학습, K-means, GMM, PCA, t-SNE를 공부하고, CNN → MobileNetV2 특징 추출 → 미세 조정의 비교 과정을 노트북과 포스터로 구성했습니다.

`Python` · `Jupyter Notebook` · `NumPy / pandas` · `Matplotlib / Seaborn`

[기초 학습 노트](docs/learning-notes.md) · [프로젝트 노트북](Project/해충_학습모델.ipynb) · [포스터 PDF](Project/해충_학습모델_포스터.pdf)

## 자료 미리보기

<a href="Project/해충_학습모델_포스터.pdf"><img src="images/pest-classification-poster.png" alt="해충 분류 PBL 포스터 미리보기" width="640"></a>

> 기존 포스터의 미리보기입니다. 포스터와 노트북의 성능 수치는 아래 설명처럼 예시로 읽어야 합니다.

## 프로젝트 구성과 현재 범위

| 자료 | 내용 |
| --- | --- |
| 기초 학습 노트 | 지도·비지도 학습, 군집화, 차원 축소 개념과 그림 |
| 해충 분류 노트북 | 5종 해충 데이터 소개, 모델 단계 설명, 비교표·그래프·리포트 예시 |
| 포스터 | 연구 배경과 모델 개선 과정을 시각적으로 요약 |

**현재 노트북의 모델 함수는 실제 신경망을 학습하는 코드가 아니라 설명용 메시지를 출력하는 구현입니다.** 정확도 `68.4% → 88.5% → 96.4%`, 추론 시간 및 혼동 행렬은 코드에 직접 입력된 예시 값입니다. 이 저장소만으로 실제 학습·평가 결과나 성능을 재현할 수는 없습니다.

분류 대상으로 소개한 해충은 갈색날개매미충, 미국선녀벌레, 썩덩나무노린재, 작은뿌리파리, 담배거세미나방입니다.

## 노트북 열기

```bash
git clone https://github.com/unknownamed/Deep-Learning-Basics.git
cd Deep-Learning-Basics
python -m venv .venv
```

Windows는 `.\.venv\Scripts\Activate.ps1`, macOS/Linux는 `source .venv/bin/activate`로 활성화합니다.

```bash
python -m pip install jupyter numpy pandas matplotlib seaborn
jupyter notebook
```

`Project/해충_학습모델.ipynb`를 열면 예시 표·그래프를 실행해 볼 수 있습니다. 한글 그래프에는 Windows의 맑은 고딕, macOS의 AppleGothic, Linux의 NanumGothic 설정을 사용합니다.

## 실제 모델 실험으로 확장할 부분

- 데이터 취득 및 전처리·학습/검증/테스트 분할
- CNN·MobileNetV2 모델 정의와 실제 학습 루프
- 모델 가중치 저장, 테스트 예측에서 계산한 지표와 혼동 행렬
- 실행 환경·데이터 버전·측정 방법 기록

기존 자료와 학습 과정은 [학습 노트](docs/learning-notes.md)에 보존했습니다.
