# Terminus AI

Terminus is the autonomous execution layer for DeepSeek Harness.

It builds on `dsh-base` rather than replacing the Harness runtime. The base
profile already provides tools, sessions, subagents, jobs, workflows, shell,
filesystem access, web search, and the guarded tool execution pipeline.

The Terminus bundle adds:

- an execution-oriented agent persona;
- explicit inspect → plan → execute → observe → recover → verify behavior;
- persistent SQLite-backed full-text session search;
- reuse-oriented instructions for prior successful work;
- the existing Harness permission boundary remains the default.

The intended composition is:

```
dsh-base
  + dsh-headless
  + dsh-terminus
```

Install this bundle into a profile named `terminus`, then run the profile
headlessly on the VPS.
