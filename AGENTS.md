# work-status

팀 업무현황 서비스. 사람용 개요는 `project.md`, AI 에 매 요청 주입되는 컨텍스트는 `openspec/config.yaml` 의 `context:`.

<!-- openspec-bootstrap:tdd -->
## 개발 규율 — TDD

모든 구현은 **실패하는 테스트(RED)** 에서 시작한다.
각 작업(`openspec/changes/<slug>/tasks.md`의 한 줄)마다:

1. **RED** — 그 작업을 표현하는 실패하는 테스트를 먼저 쓴다.
2. **GREEN** — 테스트를 통과시키는 최소 코드만 쓴다.
3. **REFACTOR** — green을 유지하며 정리한다.
4. `tasks.md` 항목을 `[x]`로 바꾸고, change 폴더의 `notes.md`에 핸드오프 한 줄을 남긴다.

규칙:
- 테스트 없는 코드는 워크플로우 위반이다.
- `tasks.md`에 없는 작업은 하지 않는다 — 필요하면 명세(단계 1)부터 고친다.
- 동결된 명세(스펙 = SOT)와 코드가 다르면 명세에 맞춘다. 명세가 틀렸으면 명세를 먼저 고친다.
<!-- /openspec-bootstrap:tdd -->
