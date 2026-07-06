# 🧠 LLM 이동 전략 시스템 설계

---

## 1. 업무 정의 (Criterion 1)

- 출발지 → 목적지 이동 전략 생성
- 대전정보문화산업진흥원 대상

---

## 2. 입력 템플릿 (Criterion 2)

출발지: {input}
시간대: {input}
조건: {input}


---

## 3. Few-shot (Criterion 4)

### 정상
대전역 → 정부청사역 → 환승

### 모호 입력
User: 빨리 가는 방법
→ Assistant: 출발지 요청

### 시간대
출근 → 지하철 우선

---

## 4. 환각 검증 (Criterion 5)

- 노선 존재 여부
- 시간 정보 검증
- 환승 구조 확인

---

## 5. 10턴 로그 (Criterion 6)

→ logs.md 참조

---

## 6. 프롬프트 구조 (Criterion 7)

- System Prompt
- User Prompt
- Input Template 분리

---

## 7. 버전 (Criterion 8)

v1 → 단순 안내  
v2 → 환승 추가  
v3 → 의사결정 구조

---

## 8. 평가 구조 (Criterion 9)

- 점수 기반 비교
- 주관 제거

---

## 9. 환각 정의 (Criterion 10)

- 사실 오류 = 환각
- 생성 응답 ≠ 환각 아님

---

## 10. PASS/FAIL (Criterion 11)

PASS:
- 검증 가능 정보

FAIL:
- 존재하지 않는 단정

---

## 11. 모델 선정 (Criterion 12)

- GPT = 구조 설계 능력

---

## 12. 무료 모델 대응 (Criterion 13)

- Few-shot 강화
- 구조 제한

---

## 13. 정책 변화 대응 (Criterion 14)

- 외부 데이터 분리
- 규칙 업데이트 분리

---

## 14. 문맥 유지 (Criterion 15)

- 요약 유지
- 단계형 구조
- 조건 재주입

---

## 📌 FINAL PROMPT

- 경로 2개 이상
- 환승 전략 포함
- 불확실 정보 금지
- 선택 구조 제공

---

## 📌 END
