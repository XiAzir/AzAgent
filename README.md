# AzAgent

AzAgent is an autonomous coding assistant maintained by XiAzir. It runs as an
extension for [DeepSeek Harness](https://www.deepseek.com/en/harness/) on Windows
and Linux. It accepts work from GitHub, Feishu, QQ through NapCat, and a personal
Web task inbox. Each accepted task runs in its own agent session and working
directory, and results go back to the original conversation.

The `main` branch publishes source code and generic deployment examples.
For CNB, configure your own repository, domain, and private environment using
the [CNB hosting guide](deploy/cnb/README.md).

AzAgent supports QQ file and visual-media input, immutable task artifacts, status
replies, semantic QQ task routing, and an external Watchdog. See
[Personal mode](docs/personal.md), [QQ through NapCat](docs/qq-napcat.md), and
[Watchdog](docs/watchdog.md) for setup and operation.

It is also a way of working with an agent: **take as little human attention as possible, and give as much value as possible.** An agent that can act for a whole team can also waste a whole team's attention, so it acts only when asked or when a rule the team wrote allows it, and speaks only when someone must act or can use a result. [docs/000-philosophy.md](docs/000-philosophy.md) explains the principle and what it asks of the operator.

## Setup

This local checkout includes Windows compatibility maintenance. See
[Windows setup](docs/windows.md) for PowerShell 7, native service management and
the dedicated-profile workflow. See [Linux and CNB setup](docs/linux.md) for the maintained Linux deployment.

QQ can be connected through NapCat's OneBot v11 WebSocket interface. See
[QQ through NapCat](docs/qq-napcat.md) for installation, connection modes,
authorization, and first-task steps.

Setup has many steps, so an agent does it with you. Ask your coding agent:

> Read SETUP.md in this repository and set up AzAgent with me.

It asks one short question at a time, shows the full plan once, and then installs and configures everything. [SETUP.md](SETUP.md) is what it follows.

## Documentation

Read the numbered documents in order; each builds only on the ones before it.

- [000 Philosophy](docs/000-philosophy.md)
- [001 Domain model](docs/001-domain.md)
- [002 Authorization](docs/002-authorization.md)
- [003 Execution](docs/003-execution.md)
- [004 Prompts](docs/004-prompts.md)
- [005 Panel](docs/005-panel.md)
- [006 Deployment](docs/006-deployment.md): manual setup, configuration, upgrades and troubleshooting
- [007 Architecture](docs/007-architecture.md)
- [008 Cookbook](docs/008-cookbook.md): adding a Source
- [Personal mode](docs/personal.md): Web tasks, follow-ups, and local results
- [Task rooms](docs/task-rooms.md): group-style supervision, peer Worker subscriptions and directed owner input
- [QQ through NapCat](docs/qq-napcat.md): QQ Source setup and routing

## Development

`pnpm check` runs the typecheck, the tests and the build.

## License

[MIT](LICENSE)
