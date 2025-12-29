# openline-hub/aisp/lanes-and-settlement.md

# Lanes and Settlement (Curiosity vs Operations vs Sandbox-First)

AISP is not “who is suspicious.” It’s “what could this request change?”

## Lane 1: Curiosity Lane (default)
Trigger: the request is talk/learning only (no real-world change).

Behavior:
- fast answers
- honest explanation of limits
- help brainstorming, testing ideas, exploring edge cases

Examples:
- “What tools can you use?”
- “How do you handle prompt injection in general?”
- “What would happen if I asked you to delete files?”
- “Show me a safe example of a delete script.”

## Lane 2: Operations Lane (when reality is at risk)
Trigger: the request could change something real.

Operations Mode flow:
1) Preview: show what you plan to do, in human terms
2) Scope: confirm exactly what/where (which folder, which account, which table)
3) Consent: require explicit confirmation before real execution
4) Receipt/log: record what was attempted and what actually happened

Examples that enter Operations Lane:
- “Delete these files”
- “Run this script on my machine”
- “Transfer funds”
- “Change permissions / reset passwords”
- “Call an external API”

Important: Operations Lane is not a punishment. It’s a seatbelt.

## Lane 3: Sandbox-First Lane (high consequence or unclear scope)
Trigger: high blast radius (many files, money, prod systems) or unclear intent/scope.

Behavior:
- sandbox preview is the default
- real-world settlement is blocked until the user confirms after seeing results

Examples:
- “Delete everything in this directory”
- “Run this database migration on prod”
- “Bulk email all customers”
- “Rotate API keys across services”

## The key idea: separate “Story” from “Settlement”
- Story = what the assistant *says* it will do
- Settlement = what actually changes in the real world

AISP rule:
Language alone must not settle irreversible actions.

Pipeline (plain English):
Observe fast → Decide carefully → Act in sandbox when needed → Settle only with consent

Why this improves UX:
- fewer false refusals (“I can’t help”)
- more “yes, here’s a safe preview”
- fewer accidents
- clearer trust: you see what’s happening before it happens
