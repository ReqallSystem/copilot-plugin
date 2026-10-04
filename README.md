# Reqall GitHub Copilot plugin

## Installation

Copy or merge `.github/copilot-instructions.md` into the target repository at the same path. Merge `.vscode/mcp.json` into its VS Code MCP configuration without overwriting existing servers. Preserve any existing repository instructions. The npm archive includes both hidden directories, but installing the npm package does not activate repository instructions automatically. Enable repository custom instructions in your Copilot host; no runtime hooks are installed.

## Project naming

Reuse a host-bound project throughout recall and persistence; explicit operation arguments (including SLEEP) remain authoritative. Otherwise use `REQALL_PROJECT_NAME` / existing host setting → network Git origin → explicitly labelled `project_name` or `project` → nearest `.reqall.yml` / `.reqall.yaml` → nearest `package.json` / `go.mod` / `Cargo.toml` → exact path relative to a known workspace → `.machine/<short-lower-hostname>/<os-user>`. Preserve explicit identifiers; never guess from a basename or an unlabelled slash token. Route account-wide preferences deliberately to `.user`.

The installed instruction assets embed the full offline policy, including metadata limits and Git compatibility. Canonical reference: https://github.com/ReqallSystem/plugins/blob/main/doc/PROJECT_NAMING.md

## Verification

Run `npm test` to check installed instructions and `npm pack --dry-run` coverage.
