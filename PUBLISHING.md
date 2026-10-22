# 공개 템플릿 배포자용 안내

원본 Private memory의 파일·커밋 이력·실제 항목은 가져오지 않습니다.

1. 별도 **Public** `memory-starter` 저장소의 `main`에 비식별 빈 구조만 배포합니다.
2. GitHub **Settings → General → Template repository**를 체크합니다.
3. 직원은 `Use this template`로 자신의 **Private `memory`**를 만들도록 안내합니다.
4. 공개 전에 README, 색인, 모든 커밋, PR, Actions 로그의 개인정보·사건 식별 단서·토큰·비공개 내용을 확인합니다.
5. 실제 직원 계정에서 Private 복제, 자기 `m1` 연결, 선택적 memory 읽기·쓰기 가능 여부를 테스트합니다.

이 저장소에 실제 기억, API 키, Secrets, 자동 수집 workflow를 추가하지 않습니다.
