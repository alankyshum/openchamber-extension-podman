# Podman extension for OpenChamber

An OpenChamber panel for inspecting and managing Podman containers, Compose stacks, images, volumes, networks, and storage. It shells out only to the `podman` CLI through OpenChamber's host execution permission.

This project is a Podman port of the MIT-licensed [OpenChamber Docker extension](https://github.com/openchamber/openchamber-extension-docker), with its original interface and Git history retained.

## Features

- List running and stopped containers, inspect metadata, and view live resource usage.
- Start, stop, restart, pause, unpause, and remove containers.
- View and search container logs, execute shell commands, and browse container files.
- Open published TCP host ports with one click.
- Group Compose containers using Podman or Docker Compose project labels.
- Inspect and manage images, volumes, networks, and Podman storage.

## Prerequisites

- OpenChamber 1.22.0 or newer.
- The `podman` CLI available on `PATH`.
- On macOS, a running Podman machine (`podman machine start`).
- Optional: a Compose provider available to `podman compose` for Compose-managed workloads. Containers still appear normally when no provider is installed.

## Installation

### Release archive

1. Download or build `podman-extension.zip`.
2. In OpenChamber, open **Settings → Extensions → Add Extension**.
3. Select the zip archive (or this extracted repository directory).
4. Approve local agent execution when prompted. The extension requests permission to execute only `podman`.

### Local checkout

Clone this repository, run `bun install && bun run bundle`, then select the repository folder from **Settings → Extensions → Add Extension**.

## Development

- `bun install` installs dependencies.
- `bun run type-check` checks the TypeScript panel.
- `bun run bundle` rebuilds `panel/main.js`.
- `bun run pack` creates `podman-extension.zip`.

## License

MIT. See [LICENSE](LICENSE).
