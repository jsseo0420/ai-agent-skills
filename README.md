# 스킬 만들기

오늘 운동한 내용 정리하기

Claude Code CLI에 프로젝트 스킬을 등록하고, 그 스킬로 헬스 운동 기록(운동 명칭, 세트 수, 세트당 횟수)을 정리하는 실습입니다.

## 폴더 구조

```
.claude/skills/workout-log/SKILL.md   # 운동 기록 정리 스킬
workouts/raw/                         # 하루 단위 운동 메모 (일주일치 가상 데이터)
workouts/summary/                     # 스킬로 정리한 주간 결과
```

## 사용 방법

1. 이 폴더에서 Claude Code를 실행합니다.

   ```bash
   claude
   ```

2. `.claude/skills/` 아래의 스킬은 자동으로 등록됩니다. 아래처럼 호출합니다.

   ```
   /workout-log 2026-10-26 ~ 2026-11-01
   ```

   "이번 주 운동 정리해줘"처럼 말로 요청해도 스킬이 적용됩니다.

3. 결과는 `workouts/summary/시작일_종료일.md`에 저장됩니다.

## 실습 결과

- 입력: [workouts/raw](workouts/raw) — 2026-10-26 ~ 2026-11-01 운동 메모 7개
- 출력: [workouts/summary/2026-10-26_2026-11-01.md](workouts/summary/2026-10-26_2026-11-01.md)
- 요약: 운동 5일 (휴식 2일), 총 71세트, 840회
