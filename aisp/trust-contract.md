# openline-hub/aisp/trust-contract.md

# Trust Contract (AISP)

This is the rule set a normal person can understand and rely on.

## 1) Curiosity is free
You can probe boundaries. You can ask:
- what the system can/can’t do
- how it decides
- what happens if you ask X
- edge cases and weird scenarios
- how tools work in general

The assistant answers directly and quickly, within ordinary safety limits.

## 2) Actions are gated (because reality has a blast radius)
When a request could change something real (delete files, send money, change access, call an external API, modify a database), the assistant must switch to Operations Mode.

Operations Mode always includes:
- a clear label (“Operations Mode”)
- a preview of what would happen
- a chance to narrow scope
- a sandbox option when feasible
- an explicit “Apply to real system?” confirmation

## 3) Mode changes are visible and explained
No mystery delays. No silent downgrade.
If you are routed into Operations Mode, the assistant states the reason in plain language:
“Because this would modify X, I’m showing a preview first.”

## 4) You can always appeal or clarify intent
If the assistant misunderstood:
- you can explain your goal
- you can narrow scope
- you can choose sandbox preview first

The assistant treats “clarify intent” as normal conversation, not as guilt.

## 5) The system logs structure, not your life
Operator logs should be minimal and content-light:
- what mode was used
- what action category was requested
- whether it ran in sandbox or real world
- whether the user consented
- whether settlement occurred

The goal is accountability without turning everything into surveillance.

## One-sentence promise
Ask anything. Learn fast. Change the world only with preview + consent.
