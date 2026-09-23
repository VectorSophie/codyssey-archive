# codyssey-archive

Codyssey 미션 저장소 모음. 각 미션은 독립 저장소이며, 여기서는 Git Submodule로
한곳에 모아둔다.

## 구조

```
codyssey-archive/
├── basic/       bX-X 미션 (14개, submodule)
├── advanced/    aX-X 미션 (10개, submodule)
└── master/      (아직 없음, .gitkeep으로 자리만 유지)
```

## 클론 방법

서브모듈까지 한 번에 받으려면:

```bash
git clone --recurse-submodules https://github.com/VectorSophie/codyssey-archive.git
```

이미 클론한 뒤라면:

```bash
git submodule update --init --recursive
```

## basic/ (bX-X)

디렉터리와 개인 과제 레포 이름은 개편된 미션 번호를 따른다. `b2-2`는 팀 저장소를 그대로 참조한다.

| 미션 | 저장소 | 주제 |
|---|---|---|
| b1-1 | [codyssey-b1-1](https://github.com/VectorSophie/codyssey-b1-1) | 개발자 포트폴리오 사이트 |
| b1-2 | [codyssey-b1-2](https://github.com/VectorSophie/codyssey-b1-2) | Bookmark Keeper |
| b2-1 | [codyssey-b2-1](https://github.com/VectorSophie/codyssey-b2-1) | 파일 기반 가계부 CLI |
| b2-2 | [Git_Collaboration](https://github.com/Im-Jongseok/Git_Collaboration) | Git 협업 실습 (3인 팀, 외부 저장소) |
| b3-1 | [codyssey-b3-1](https://github.com/VectorSophie/codyssey-b3-1) | AWS 웹 서비스 인프라 구축 |
| b3-2 | [codyssey-b3-2](https://github.com/VectorSophie/codyssey-b3-2) | AI 기반 Git 커밋/PR 자동 생성기 |
| b4-1 | [codyssey-b4-1](https://github.com/VectorSophie/codyssey-b4-1) | Linux 서버 운영 및 자동화 |
| b4-2 | [codyssey-b4-2](https://github.com/VectorSophie/codyssey-b4-2) | 시스템 장애 분석 |
| b5-1 | [codyssey-b5-1](https://github.com/VectorSophie/codyssey-b5-1) | Mini Redis (자료구조 직접 구현) |
| b5-2 | [codyssey-b5-2](https://github.com/VectorSophie/codyssey-b5-2) | Mini Git — CLI 기반 커밋 그래프 엔진 |
| b6-1 | [codyssey-b6-1](https://github.com/VectorSophie/codyssey-b6-1) | 온라인 서점 DB (bookstore) |
| b6-2 | [codyssey-b6-2](https://github.com/VectorSophie/codyssey-b6-2) | FastAPI 메모장 (라우터/서비스/저장소 계층 분리) |
| b6-3 | [codyssey-b6-3](https://github.com/VectorSophie/codyssey-b6-3) | 도서 대여 서비스 — 인증/인가 + 연관관계 확장 |
| b7-1 | [codyssey-b7-1](https://github.com/VectorSophie/codyssey-b7-1) | EVERYTHING (풀스택 웹 서비스) |

## advanced/ (aX-X)

| 미션 | 저장소 | 주제 |
|---|---|---|
| a1-1 | [codyssey-a1-1](https://github.com/VectorSophie/codyssey-a1-1) | 이커머스 멀티모달 데이터 분석 + RFM 고객 세분화 |
| a2-1 | [codyssey-a2-1](https://github.com/VectorSophie/codyssey-a2-1) | AI 수학 기반: 선형대수 · 미적분 · 최적화 · 확률통계 |
| a3-1 | [codyssey-a3-1](https://github.com/VectorSophie/codyssey-a3-1) | 문서 스캐너 (OpenCV + NumPy) |
| a3-2 | [codyssey-a3-2](https://github.com/VectorSophie/codyssey-a3-2) | 모션 추적 & 특징점 재인식 (OpenCV) |
| a4-1 | [codyssey-a4-1](https://github.com/VectorSophie/codyssey-a4-1) | TF-IDF 문서 검색 & 분류 (NumPy 직접 구현) |
| a4-2 | [codyssey-a4-2](https://github.com/VectorSophie/codyssey-a4-2) | 규칙 기반 정보 추출 + 감성 분석 |
| a5-1 | [codyssey-a5-1](https://github.com/VectorSophie/codyssey-a5-1) | 신용 리스크 ML 파이프라인 (규칙 기반 vs 머신러닝) |
| a5-2 | [codyssey-a5-2](https://github.com/VectorSophie/codyssey-a5-2) | 고객 군집화 + XAI 신용 리스크 설명 |
| a6-1 | [codyssey-a6-1](https://github.com/VectorSophie/codyssey-a6-1) | NumPy 미니 딥러닝 프레임워크 (AutoGrad + Gradient Checking) |
| a6-2 | [codyssey-a6-2](https://github.com/VectorSophie/codyssey-a6-2) | 성능 진단·개선 파이프라인 (Few-shot 전이학습 + 시계열 예측) |

## master/

아직 미션이 없다. `.gitkeep`으로 폴더만 비워둔 채 유지한다.

## 서브모듈 업데이트

각 미션 저장소에 새 커밋이 생기면, 이 저장소에서 포인터를 갱신해야 반영된다:

```bash
git submodule update --remote --merge   # 모든 서브모듈을 각 저장소의 최신 커밋으로
git add basic advanced
git commit -m "submodule: 최신 커밋으로 갱신"
```
