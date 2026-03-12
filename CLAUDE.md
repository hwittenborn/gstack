# gstack development

## Commands

```bash
bun install          # install dependencies
bun test             # run integration tests (browse + snapshot)
bun run dev <cmd>    # run CLI in dev mode, e.g. bun run dev goto https://example.com
bun run build        # compile binary to skills/browse/dist/browse
```

## Project structure

```
gstack/
├── .claude-plugin/  # Plugin marketplace config
│   ├── plugin.json  # Plugin manifest
│   └── marketplace.json
├── skills/          # All skills (auto-discovered by plugin system)
│   ├── browse/      # Headless browser CLI (Playwright)
│   │   ├── src/     # CLI + server + commands
│   │   ├── test/    # Integration tests + fixtures
│   │   └── dist/    # Compiled binary
│   ├── ship/        # Ship workflow skill
│   ├── review/      # PR review skill
│   ├── plan-ceo-review/ # /plan-ceo-review skill
│   ├── plan-eng-review/ # /plan-eng-review skill
│   └── retro/       # Retrospective skill
└── package.json     # Build scripts for browse
```

## Installation

```
/plugin marketplace add garrytan/gstack
/plugin install gstack@gstack-marketplace
```
