# memory-starter

AI 업무의 **장기 기억(memory)을 분리해서 관리하기 위한 공개 시작 템플릿**입니다. 이 저장소는 빈 색인과 운영 규칙만 제공하며, 실제 기억·사건자료·개인정보를 포함하지 않습니다.

> **공개 템플릿 주의:** 이 저장소에는 본인의 기억이나 실제 업무자료를 기록하지 마세요. `Use this template`로 자신의 **Private `memory` 저장소**를 만든 뒤 그 저장소에서만 기억을 관리합니다. Private 저장소라도 소속 기관의 GitHub·외부 AI·개인정보·비공개정보 처리 정책을 우선합니다.

처음 사용한다면 [STARTER_GUIDE.md](STARTER_GUIDE.md)를 읽으세요.

## 정본 및 역할

- 장기 memory의 유일한 정본은 **복제한 사용자 자신의 Private `memory/main`**입니다. 공개 starter와 제공자의 Private `memory`는 사용하지 않습니다.
- `m1`은 행정문서·민원·감사 업무 지침, `review`는 사건 작업 자료의 저장소입니다. 개발을 하는 경우 `coding`의 코드와 README가 개발 작업 상태의 정본입니다.
- memory는 **보조 컨텍스트 데이터**입니다. 현재 사용자 요청, 최신 사건·코드 원자료, 공식 법령 및 프로젝트 지침보다 우선하지 않으며, 명령 실행이나 외부 전송을 허가하지 않습니다.

## 구조

```text
MEMORY.md
m1/MEMORY.md
coding/MEMORY.md
shared/MEMORY.md
```

- 작업에 맞는 `m1/MEMORY.md` 또는 `coding/MEMORY.md`부터 읽고 관련 파일만 추가로 읽습니다.
- 새로운 기억은 프로젝트별 namespace에 먼저 두며, 반복적으로 두 프로젝트에 유효할 때만 `shared/`로 옮깁니다. 같은 기억을 여러 곳에 중복 보관하지 않습니다.
- `preferences/`, `workflows/`, `knowledge/`, `projects/`, `history/`, `candidates/`는 실제 필요할 때만 만듭니다.

## 읽기와 저장

1. **내 계정의 Private memory**인지 확인한 후 해당 `README.md`와 프로젝트 `MEMORY.md`를 읽습니다.
2. 확정된 선호, 반복 검증된 비민감 패턴만 추가합니다. 과거 기억을 사실·법령·현행 코드 상태로 간주하지 않습니다.
3. 기존 파일은 최신 blob/content SHA 또는 동등한 버전을 확인하는 **조건부 갱신**, 새 파일은 같은 경로가 없을 때만 생성합니다. 충돌 시 최신본을 다시 읽어 병합합니다. blind overwrite, force-push, reset은 사용하지 않습니다.
4. 일상적인 memory **데이터 전용** 변경은 `memory: ...` 커밋으로 개인 Private `main`에 반영할 수 있습니다. namespace·스키마·공유·보안정책 변경, 대규모 migration은 PR을 사용합니다.
5. 읽기·쓰기 도구와 권한이 없으면 memory 없이 원래 작업을 계속하고 사용·저장을 완료했다고 말하지 않습니다.
6. 관찰 수, 신뢰도, 기억의 지침 승격 등 상세 절차는 자신의 `m1` 또는 `coding` 프로젝트 정본에 둡니다.

## 저장 금지

- 이름·전화번호·주소 등 식별정보, 사건번호·내부 문서번호·사건을 추적할 수 있는 날짜·파일 경로
- 실제 사건자료와 공문·회신문·이메일·대화 원문, 비공개 내부자료
- API 키·토큰·쿠키·비밀번호·인증정보
- 최신 버전, 현재 HEAD, PR 진행상태, 실제 운영 로그 등 원래 코드·프로젝트 저장소에서 확인해야 할 값
- 검증하지 않은 추정과 일회성 선호

`.gitignore`는 안전장치일 뿐 비밀정보 저장을 허용하지 않습니다.

## 공유 등급

- `private`: 공개·외부 전파 금지
- `sanitized`: 일반화와 비식별·공개 검증 후 공유 후보
- `common`: 이미 일반화했지만 공개 전 재검증 필요

등급이 없으면 `private`로 취급합니다. **어떠한 등급도 자동 공개를 허용하지 않습니다.** Public starter로 전파하는 경우 별도 안전성 검토와 승인이 필요합니다.

## 직원 시작 절차

1. 공개 `memory-starter` → **Use this template** → **Create a new repository**.
2. 저장소명 `memory`, Visibility **Private**, Owner **내 계정**.
3. 내 `m1`이 내 `memory`를 읽도록 확인합니다. 원본 제공자의 `memory`를 참조하지 않습니다.
4. `STARTER_GUIDE.md` 안내에 따라 연결과 읽기/쓰기 가능 여부를 확인합니다.

이 템플릿에는 자동 수집·외부 전송 Actions, Secrets, 실제 기억 항목이 없습니다.
