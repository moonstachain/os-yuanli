# OS-原力

`os-yuanli` is a standalone root skill for running work through `治理OS × 工作OS`.

It is designed to:

- start from `六判断`
- pass through `主题层 -> 策略层 -> 执行层`
- adapt outputs by task family
- verify before claiming completion
- end with an `Evolution Note`

## Repository Structure

- `SKILL.md`: the root operating protocol
- `agents/openai.yaml`: UI-facing metadata
- `references/`: compact constitutions, routing bridges, output contracts, and audit playbooks
- `scripts/doctor.py`: static checks for this repository copy

## Intended Usage

Use this repository as the GitHub-published source for the `os-yuanli` skill.

The local installed skill may still live under `$CODEX_HOME/skills/os-yuanli`. This repository is the clean, shareable mirror of that skill rather than the canonical runtime home.

## Dependency Model

`os-yuanli` is a root protocol. It expects a Codex skill environment with several downstream skills available, such as:

- `intent-grounding`
- `skill-router`
- `jiyao-youyao-haiyao-zaiyao`
- `evidence-gate`
- `closure-evolution`

The exact integration contract is documented in [references/integration-boundaries.md](references/integration-boundaries.md) and [references/routing-bridges.md](references/routing-bridges.md).

## Validation

Run:

```bash
python3 scripts/doctor.py
```

This checks repository structure, key protocol tokens, and reference integrity for the published copy.
