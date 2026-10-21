# UP77TRADER 분석 저장소

업비트 KRW 자동매매 봇 UP77TRADER의 성과를 분석하고 개선하는 저장소입니다.

## 목표
MDD 20% 이하 조건에서 수수료·슬리피지 차감 후 거래당 기대값을 최대화한다.

## 작업 방식
- 거래 분석 요청은 `trade-analyst` 에이전트가 수행하고, 결론을 내기 전에 `trade-critic` 에이전트가 독립 검토한다.
- 모든 판단 기록은 `journal/`에 누적한다.
  - `lessons.md`: 반복 금지 실수
  - `hypotheses.md`: 사전 등록된 가설과 검증 결과
  - `decisions.md`: 실제 적용한 변경과 쿨다운
  - `calibration.md`: 예측 적중률(메타인지)
- 보고서는 `reports/YYYY-MM-DD.md`에 저장한다.
- 입력 데이터는 `data/raw/`에 둔다. 형식은 `data/README.md` 참고.

## 금지
- `.env`, API 키를 읽거나 커밋하지 않는다.
- 실거래 설정·코드를 사람 승인 없이 변경하지 않는다.
