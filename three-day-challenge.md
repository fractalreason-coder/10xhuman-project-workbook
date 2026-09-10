# AI로 내 반복업무 하나 바꾸기 · 3일 미니 챌린지

**AI를 배웠다는 말보다, 직접 써본 결과물 하나.**

10xhuman 운영팀이 만든 무료 자기주도 실습입니다. 하루 한 단계씩, 필요하면 더 천천히 진행하세요. 3일은 권장 진행 순서이며 완성·매출을 보장하는 기간이 아닙니다.

[가입 없이 무료 기획서 시작하기](https://10xhuman.net/start?lang=ko&utm_source=github&utm_campaign=project_clinic)

무료 기획서에는 카드 입력이 없습니다. 아래 실습 자료도 무료입니다. Astra·Claude Code 등 외부 도구 이용료는 각 서비스 조건에 따릅니다. 이 실습은 299,000원·12개월 온라인 과정 전체 이용권이나 코칭 프로그램이 아닙니다.

## Day 1 — 오늘 귀찮았던 일 하나

이번 주 반복한 일 세 가지를 적고, 가장 작은 것 하나를 고르세요.

- 같은 질문에 답변하기
- 흩어진 메모를 정리하기
- 비교할 정보를 표로 옮기기

무료 기획서의 세 질문에 자신의 상황을 적습니다. 마지막에는 다음 문장을 완성하세요.

> 나는 [누구]가 [반복하는 일]을 할 때 겪는 [불편]을 줄이기 위해 [작은 도구]를 만든다.

**연습용 가상 예시:** 혼자 서비스를 운영하는 사람이 자주 받는 문의를 분류하고, 확인된 FAQ에서 답변 초안을 찾는 도구. 실제 수강생이나 고객 사례가 아닙니다.

오늘의 결과: 내려받은 기획서 하나. 기능은 문의 입력 → 분류 → 수정 가능한 답변 초안 표시까지만 잡습니다.

## Day 2 — AI에게 맡기되, 내가 범위를 정하기

기획서와 아래 프롬프트를 Astra 또는 Claude Code에 전달하세요. 아래 예시는 실습용입니다. 개인정보 없이 가상의 문의만 사용합니다.

```text
첨부한 기획서를 바탕으로 내가 직접 실행해볼 최소 제품을 구현해줘.
목표: 문의 한 건을 입력하면 유형과 답변 초안을 보여주는 연습용 도구.

이번 버전의 범위:
1. 문의 입력창, 분류 버튼, 결과 영역.
2. 입력이 비면 안내하고 결과를 생성하지 않기.
3. 아래 가상 FAQ와 명확히 일치할 때만 답변 초안을 표시하기.
   - 이용 시간: 평일 10:00~18:00
   - 예약 변경: 가상 서비스의 예약 변경은 담당자 확인 필요
4. 모르는 질문은 '확인이 필요합니다'로 표시하기.
5. 초안은 사용자가 수정·복사할 수 있게 하기.
6. 실제 이메일 발송, 결제, 개인정보 저장, 외부 AI API 연결은 넣지 않기.
7. 초기 버전은 로컬 규칙 기반으로 구현하고, 이를 AI 추론이라고 표시하지 않기.

먼저 구현 범위와 가정을 짧게 설명한 다음 구현해줘.
실행 방법, 아래 테스트 결과, 아직 확인하지 못한 점을 함께 알려줘.
실제 실행하지 못한 테스트는 통과했다고 하지 마.
내가 이해할 수 있게 주요 파일과 수정 위치를 설명해줘.
```

자기 문제로 바꿀 때는 목표·입력·출력·하지 않을 일을 바꾸세요. AI가 준 설명을 읽고, 직접 입력해서 결과를 확인합니다.

오늘의 결과: 로컬에서 실행 가능한 작은 화면과 실행 방법. 공개 배포는 아직 필수가 아닙니다.

## Day 3 — 잘된 장면뿐 아니라 틀린 장면도 확인하기

| 입력 | 기대하는 동작 | 실제 결과 |
|---|---|---|
| 빈 입력 | 내용을 입력하라는 안내 | 직접 기록 |
| 몇 시까지 이용할 수 있나요? | 평일 10:00~18:00 초안 | 직접 기록 |
| 예약을 변경하고 싶어요 | 담당자 확인 필요 안내 | 직접 기록 |
| 환불을 보장해 주세요 | 확인이 필요합니다. 정책을 지어내지 않음 | 직접 기록 |

틀린 동작이 있으면 입력·기대 결과·실제 결과를 AI에게 함께 전달해서 고칩니다. 최소 한 번은 수정 후 같은 입력으로 다시 확인하세요.

### 나의 변화 기록

- 전에는: 어떤 일이 막혔나요?
- 지금은: 내가 직접 실행하고 설명할 수 있는 것은 무엇인가요?
- AI가 맡은 부분:
- 내가 정하고 수정한 부분:
- 직접 확인한 입력과 결과:
- 아직 안 되는 것:
- 다음에 실제 사용자에게 확인할 질문 하나:

[막힌 지점이나 첫 시도에 피드백 요청하기](https://github.com/fractalreason-coder/10xhuman-project-workbook/issues/1)

기획서만 완성했어도 참여할 수 있습니다. 공개해도 되는 목표·시도·질문 하나만 남겨주세요. 피드백은 비동기이며 AI 어시스턴트가 작성할 수 있습니다. 비공개 정보나 인증키는 올리지 마세요.

공개 후기나 성공담 작성은 필수가 아닙니다. 이 실습을 마쳤다는 이유만으로 수료 인증이 발급되지 않습니다. 전체 과정의 무료 100명 초대는 실제 신청·발급 경로가 준비된 뒤 별도로 안내합니다.

---

## English — One recurring task, one small prototype

A free, self-directed exercise from the 10xhuman team. Three days is a suggested sequence, not a delivery or income guarantee.

1. **Define:** [Create a free brief without signup](https://10xhuman.net/start?lang=en&utm_source=github&utm_campaign=project_clinic). Choose one repeated task and one useful output.
2. **Build:** Give your brief to your coding assistant. Request a minimal local prototype, explicit assumptions, run instructions and no paid API integration. A rules-based prototype is a valid start; label it honestly.
3. **Check:** Try a normal input, an empty input and an unknown question. Record expected versus actual behavior, fix one issue, and explain your contribution.

Example, not a learner story: a small FAQ draft helper that only uses supplied facts and flags unknown questions for review. Do not send replies automatically.

[Share one attempt or ask one question](https://github.com/fractalreason-coder/10xhuman-project-workbook/issues/1). The brief and exercise are free; external coding tools have their own terms. This is not full-course access, human coaching or automatic certification. Public testimonials are optional.
