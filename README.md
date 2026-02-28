# Delphi

*The Oracle that foresees all outcomes.*

A skill for coding agents that generates and executes comprehensive test scenarios — **guided cases** — covering positive, negative, edge, accessibility, and security paths for any software.

## Install

```bash
ln -sf /path/to/delphi/skills/delphi ~/.claude/skills/delphi
```

## Usage

### Generate guided cases

After building software, invoke Delphi to generate test scenarios:

```
Generate guided cases for this project
Generate guided cases for the auth flow
Write test scenarios for the checkout module
```

Delphi will:
1. Analyze your code, docs, and running app
2. Discover testable surfaces (UI, API, CLI, background)
3. Present a surface map for your confirmation
4. Generate structured Markdown cases to `tests/guided-cases/`

### Execute guided cases

Run generated cases via browser automation or programmatic verification:

```
Execute guided cases
Run P0 guided cases
Execute UI cases for auth
```

Delphi will execute each case step-by-step, capture evidence (screenshots, API responses), and generate a report to `tests/guided-cases/reports/`.

### Pipeline integration

Add to your `pipelines.yaml` (for [skill-conductor](https://github.com/your/skill-conductor)):

```yaml
skills:
  delphi:
    source: external
    phase: verify
    type: phase

pipelines:
  feature:
    phases: [explore, plan, build, verify, review, finish]
    skills:
      verify:
        - verification-before-completion
        - delphi
```

## Output format

Each guided case is a structured Markdown file. See `examples/` for reference.

## Docs

- [Vision & Scope](docs/VISION.md) — full project vision
- [Design](docs/plans/2026-02-27-delphi-design.md) — architecture decisions
