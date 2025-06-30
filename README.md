## 📌 0. 프로젝트 개요
> 멋쟁이사자처럼 5기 파이널 프로젝트 신용카드 고객 세그먼트 분류 프로젝트
>
> 팀기반 데이터 분석 프로젝트 (2025) 
>
> 신용카드 고객 데이터를 기반으로, 고객을 세그먼트별로 분류하는 머신러닝 프로젝트입니다.
>
> 원 대회 : https://dacon.io/competitions/official/236460/overview/description
>
> 파이널프로젝트 제출 링크 : https://www.kaggle.com/competitions/likelioneda5thfinalproject


---

### **!참여자 분들은 잊지 마시고 root/docs/first_time_setup.md를 참고해서 셋팅해주세요!**

---

## 📁 프로젝트 구조

```plaintext
📦 프로젝트 루트
├── data/                      # 원본 및 가공 데이터 (Git 추적 제외)
│   ├── train/
│   │   ├── 0.종합본/           # concat해둔 데이터 저장
│   │   └── ...
│   └── test/
│       ├── 0.종합본/           # concat해둔 데이터 저장
│       └── ...
├── members/                   # 팀원별 개인 작업 디렉토리
│   ├── 안성겸/
│   │   ├── notebook/          # EDA, 모델링 노트북
│   │   ├── model/             # 모델 저장
│   │   ├── result/            # 예측 결과
│   │   ├── visualization/     # 시각화 정리
│   │   └── summary/           # 회고, 요약 정리
│   ├── 이수봉/
│   │   ├── notebook/          # EDA, 모델링 노트북
│   │   ├── model/             # 모델 저장
│   │   ├── result/            # 예측 결과
│   │   ├── visualization/     # 시각화 정리
│   │   └── summary/           # 회고, 요약 정리
│   ├── 장주호/
│   │   ├── notebook/          # EDA, 모델링 노트북
│   │   ├── model/             # 모델 저장
│   │   ├── result/            # 예측 결과
│   │   ├── visualization/     # 시각화 정리
│   │   └── summary/           # 회고, 요약 정리
│   └── 정현아/
│       ├── notebook/          # EDA, 모델링 노트북
│       ├── model/             # 모델 저장
│       ├── result/            # 예측 결과
│       ├── visualization/     # 시각화 정리
│       └── summary/           # 회고, 요약 정리
├── 📁 docs/
│   └─── first_time_setup.md
├── .gitignore                 # 추적 제외 파일 설정
└── README.md                  # 프로젝트 개요 (본 파일)
```
## 🔄 2. 작업 흐름

1. 자신의 폴더(`members/이름/`)에서 분석 진행
2. 분석 노트북 저장은 `notebooks/` 폴더에
3. 결과 시각화 및 요약은 각각 `visualization/`, `summary/`에 정리

## ✅ 3. commit rule
- <타입>: <간단한 요약> (선택적으로 상세 설명은 커밋 본문에서 작성)

### ex)
- feat: name1 EDA 초기 notebook 업로드
- fix: name3 시각화 누락된 축 레이블 수정
- refactor: name2 전처리 코드 함수화
- docs: 프로젝트 구조 README에 추가

## 🗂️ 4. commit type 종류
| 타입         | 설명                            | 예시                               |
| ---------- | ----------------------------- | -------------------------------- |
| `feat`     | 새로운 분석 또는 기능 추가               | `feat: name1 연령대별 분포 시각화 추가`     |
| `fix`      | 버그, 오류 수정                     | `fix: name2 분석에서 인덱스 오류 수정`      |
| `refactor` | 코드 구조 개선, 리팩토링                | `refactor: name3 시각화 함수로 분리`     |
| `docs`     | 문서, 발표자료, 주석 설명 추가/수정         | `docs: 발표자료 링크 추가`               |
| `data`     | 데이터 파일 추가 또는 갱신               | `data: processed 폴더에 csv 최신 업로드` |
| `style`    | 코드 포맷팅, 셀 정리, 주석, 들여쓰기 등      | `style: name1 노트북 내 셀 정리`        |
| `test`     | 임시 코드, 실험용 파일 업로드             | `test: name2 draft notebook 업로드` |
| `chore`    | 설정파일 등 기타 잡무                  | `chore: .gitignore 추가`           |
| `infra`    | 도커, 경로설정, 개발환경 구성 관련          | `infra: docker-compose 포트 재설정`   |
| `config`   | `.env`, `.yaml`, 파라미터 세팅 수정 등 | `config: 실험용 config.yaml 경로 수정`  |
| `exp`      | 실험 분기 생성, 하이퍼파라미터 튜닝 시도 등     | `exp: Segment D 전용 모델 실험 시작`     |
| `revert`   | 잘못된 커밋 롤백                     | `revert: 불필요한 모델 아웃풋 제거`         |
| `merge`    | 브랜치 병합 관련 기록                  | `merge: dev → main 브랜치 병합`       |

### ✅ commit 할 때 email은 따로 제한하지 않고 name만 본인의 이름으로 commit해주시면 됩니다.


## 🌿 5. 브랜치 전략 안내

본 프로젝트는 **개인별 브랜치 → 개인 메인 브랜치 → 최종 병합** 방식으로 관리됩니다.

### 📌 6. 브랜치 네이밍 규칙

- `이름/main`
  → 개인의 **확정 커밋만 정리**되는 메인 브랜치
  → 발표/제출 시 여기에 내용 정리
  → 당일 업무 내용은 여기 정리해주시고 매일 매일 제가 main branch로 모아드리겠습니다
- `이름/(workflow)` 
  → 개인이 자유롭게 실험/작업하는 워킹 브랜치
  → 이름을 자유롭게 사용하시어 여러 명령어를 연습할 기회가 되셨으면 좋겠습니다
  → push, reset, stash 등 자유롭게 사용 가능

> 예시:
> - `장주호/main`
> - `장주호/eda-1`
> - `장주호/workflow`
> - `장주호/plot-fix`

---

### 🔄 7. 작업 흐름

a. 작업 시작 시:
   ```bash
   git checkout -b 이름/(workflow)
   ```
b. 작업 중 커밋/수정

c. 작업 정리 완료 후:
```bash
git checkout 이름/main
git merge 이름/workflow
```

### 📋 8. 규칙 요약
| 브랜치 이름                 | 용도               | 병합 대상                 |
| --------------------------- | ------------------ | ------------------------  |
| 이름/(workflow)             | 실험, 분석, 시각화 | 직접 `이름/main`으로 병합 |
| 이름/main                   | 개인 발표용 정리본 | 최종 통합 브랜치로 병합   |
| master or main-presentation | 팀 전체 발표용     | (관리자만 병합)           |

## 9. 📁 파일 이름 규칙 (권장)

팀원 자율을 최대한 존중하지만,  
리포 구조의 일관성과 리뷰 효율을 위해 다음과 같은 파일명 형식을 **권장**합니다.

### 🔍 분석 노트북 (notebooks/)
- `01_(주제명)_EDA_기본통계.ipynb`
- `02_(주제명)_EDA_시각화.ipynb`
- `03_(주제명)_모델링_초안.ipynb`
- `00_(주제명)_정리용_최종본.ipynb`

### 📊 시각화 파일 (visualization/)
- `(주제명)_dist_age_group.png`
- `(주제명)_corr_heatmap.png`
- `(주제명)_boxplot_outliers.png`

### 📄 요약 문서 (summary/)
- `(주제명)_summary_stats.md`
- `(주제명)_insight_notes.md`
- `(주제명)_피드백_반영_요약.md`

> 📌 **팁:** 접두 숫자(`01_`, `02_`)를 붙이면 자연스럽게 작업 순서대로 정렬됩니다
