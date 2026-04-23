# Opera Dead-Stock Tracker

스킨이데아 이슈재고 소진 TF 트래커.

- **공개 URL**: https://jay-chung-ms.github.io/Opera-Dead-Stock-Tracker/
- **원본 데이터**: `260223_SI_Value up_P2E_이슈재고 분석(260405)_r7.xlsx` (기준일 2026-04-21)
- **총 대상**: 62개 SKU / 15.31억 (검토제외 별도)

## 데이터 업데이트

엑셀이 새 버전으로 갱신되면 아래 스크립트로 JS 재생성:

```bash
python scripts/build_dead_stock_data.py "경로/이슈재고 분석.xlsx"
git add data/dead_stock_tracking.js
git commit -m "데이터 갱신 YYYY-MM-DD"
git push
```

## 주의

- 입력값은 각 사용자의 **브라우저 localStorage**에 저장됩니다. 크로스 유저 실시간 공유 안 됩니다.
- 주간 취합은 "📥 내 팀 SKU 목록 다운로드" CSV를 담당자가 병합하는 방식.
- 검색엔진 인덱싱 차단(`noindex`) 적용됨.
