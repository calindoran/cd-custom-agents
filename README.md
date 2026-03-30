# Custom Agents

This repository is a Copilot plugin bundle for my personal custom agents and skills. It follows the Awesome Copilot-style layout so the content can be discovered and installed as a plugin.

## Contents

- [agents/unit-test-maintainer.agent.md](agents/unit-test-maintainer.agent.md): a unit-test focused agent for Vitest/Jest work.
- [skills/javascript-typescript-vitest-jest/SKILL.md](skills/javascript-typescript-vitest-jest/SKILL.md): shared guidance for JavaScript and TypeScript test authoring.
- [.github/plugin/plugin.json](.github/plugin/plugin.json): canonical plugin metadata used for discovery.

## Install

Publish this repository to a Git host that your Copilot environment can reach, then install it through the Copilot/VS Code plugin flow using the repository source.

## Layout

- `agents/`: custom agent prompts in `.agent.md` format.
- `skills/`: reusable skills in `SKILL.md` format.
- `.github/plugin/`: plugin metadata consumed by the plugin layout.

## Notes

Keep the paths in [.github/plugin/plugin.json](.github/plugin/plugin.json) aligned with the actual files in this repository. That file is the source of truth for the bundle.
