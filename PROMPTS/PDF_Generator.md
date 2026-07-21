# Prompt: 주간 PDF 세트 생성

## 사용 시점

주간 학습 사이클 마지막 단계. [TEMPLATES/](../TEMPLATES/)의 레이아웃을
사용해 그 주에 생성된 마크다운 콘텐츠를 6종 PDF로 변환한다.

## 입력

- `WEEKLY/WeekNN/01_Elementary.md` ([Generate_Elementary.md](Generate_Elementary.md) 결과)
- `WEEKLY/WeekNN/02_Middle.md` ([Generate_Middle.md](Generate_Middle.md) 결과)
- `WEEKLY/WeekNN/03_Parents.md` ([Generate_Parents.md](Generate_Parents.md) 결과)
- `WEEKLY/WeekNN/04_Family_Discussion.md` ([Discussion.md](Discussion.md) 결과)

## 추가로 이 단계에서 생성하는 콘텐츠

원본 기획(`Family_Learning_OS_v1.0.md`)의 PDF 구성에는 아래 2종도
포함되어 있으나, 별도 생성 프롬프트가 분리되어 있지 않으므로 이
단계에서 함께 생성한다.

- **05_Parents_Guide** — 이번 주 주제에 대한 부모용 진행 가이드
  (좋은 질문 목록, 예상 어려움, 시간 배분 제안)
- **06_Family_Newsletter** — 이번 주 요약 + 다음 주 예고 + 가족 활동
  기록 한 장 요약

## 프롬프트 템플릿

```
다음 마크다운 파일들을 각각 대응하는 TEMPLATES/*.pdf 레이아웃에 맞춰
PDF로 변환해줘.

- 01_Elementary.md → TEMPLATES/Elementary 레이아웃
- 02_Middle.md → TEMPLATES/Middle 레이아웃
- 03_Parents.md → TEMPLATES/Parents 레이아웃
- 04_Family_Discussion.md → TEMPLATES/Discussion 레이아웃
- (신규) 05_Parents_Guide, 06_Family_Newsletter는 위 "부모용 진행
  가이드" / "가족 뉴스레터" 내용을 생성한 뒤 Parents 레이아웃 계열로 변환

출력 파일명 규칙: WEEKLY/WeekNN/0X_이름.pdf
```

## 결과물 저장 위치

`WEEKLY/WeekNN/01_Elementary.pdf` ~ `06_Family_Newsletter.pdf`
