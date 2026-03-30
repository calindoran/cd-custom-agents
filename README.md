# Custom Agents

This repository is a Copilot plugin bundle for my personal custom agents and skills. It follows the Awesome Copilot plugin layout so the content can be discovered, installed, and managed as a single unit.

## Contents

- [agents/unit-test-maintainer.agent.md](agents/unit-test-maintainer.agent.md): a unit-test focused agent for Vitest/Jest work.
- [skills/javascript-typescript-vitest-jest/SKILL.md](skills/javascript-typescript-vitest-jest/SKILL.md): shared guidance for JavaScript and TypeScript test authoring.
- [.github/plugin/plugin.json](.github/plugin/plugin.json): canonical plugin metadata used for discovery.

## What's inside

This bundle contains:

- Custom agents in [agents/](agents) as `.agent.md` files.
- Skills in [skills/](skills) as self-contained folders with `SKILL.md`.
- Plugin metadata in [.github/plugin/plugin.json](.github/plugin/plugin.json).

## Install

You can install this repository as a plugin once it is published to a Git host your Copilot environment can reach.

For local testing, load it directly from a directory:

```bash
copilot --plugin-dir /path/to/Custom\ Agents
```

If you publish it to a marketplace or supported repository source, install it through the Copilot plugin workflow from there.

## Typical plugin shape

This repository follows the structure shown in the Awesome Copilot install guide:

```text
Custom Agents/
├── .github/
│   └── plugin/
│       └── plugin.json
├── agents/
│   └── unit-test-maintainer.agent.md
├── skills/
│   └── javascript-typescript-vitest-jest/
│       └── SKILL.md
└── README.md
```

## How it works

Once installed, the plugin makes the bundled agents and skills available to Copilot automatically:

- Agents appear in the agent picker and can be invoked by name.
- Skills load when their descriptions match the current task.
- The bundle stays versioned through [.github/plugin/plugin.json](.github/plugin/plugin.json).

## Layout

- [agents/](agents): custom agent prompts in `.agent.md` format.
- [skills/](skills): reusable skills in `SKILL.md` format.
- [.github/plugin/](.github/plugin): plugin metadata consumed by the plugin layout.

## Notes

Keep the paths in [.github/plugin/plugin.json](.github/plugin/plugin.json) aligned with the actual files in this repository. That file is the source of truth for the bundle.
