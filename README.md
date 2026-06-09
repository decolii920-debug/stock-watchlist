# Stock Watchlist

관심 주식 종목 리스트와 오늘의 종가/투자 정보를 한 화면에서 분석하는 정적 웹앱.

## 주요 기능

- 종목명 또는 6자리 코드로 종목 추가 (localStorage 저장)
- 체크 / 삭제 / 카운트 표시
- **분석 버튼**: 모달에서 다음 정보 표시
  - 오늘 종가 (또는 장중 현재가)와 등락 (액수 / %)
  - 전일 종가, 당일 고가/저가, 거래량
  - 52주 최고/최저
  - 룰 기반 단순 투자 시그널 (매수 관심 / 관망 / 차익 실현 고려)
- 한국 주요 40여 종목 이름→티커 자동 매핑 (KOSPI `.KS` / KOSDAQ `.KQ`)
- 6자리 종목코드 입력 시 `.KS` 실패 → `.KQ` 자동 폴백
- 미국 주식 영문 티커도 입력 가능 (예: `AAPL`, `MSFT`)

## 데이터 소스

Yahoo Finance Chart API를 [corsproxy.io](https://corsproxy.io/) 경유로 호출합니다.
프록시가 일시적으로 느리거나 응답하지 않을 수 있으며, 본 페이지는 투자 권유가 아닙니다.

## 배포

GitHub Pages 정적 호스팅. 활성화 후 다음 URL로 접근:

```
https://decolii920-debug.github.io/stock-watchlist/
```

## 로컬 실행

```
open index.html
```

별도 빌드 도구 없음. 단일 HTML 파일.
