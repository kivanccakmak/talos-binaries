# talos-binaries

Public binary releases for the Talos platform.

This repo holds **release artifacts only** — source code lives on GitLab at
<https://gitlab.com/kivanccakmak/talos>.

## What's published here

| Component | Description | Platforms |
|---|---|---|
| `talcli` | Talos CLI + MCP server (Go) | darwin/linux/windows × arm64/amd64 |
| `talos-label-printer` | Desktop label-printing app (Electron) | macOS `.dmg`, Windows `.exe`, Linux `.AppImage` / `.deb` |
| `talos-mobile.apk` | Android build of the Talos mobile app | android |

iOS builds are published to the App Store / TestFlight, not here.

## Quick install

### Homebrew (macOS / Linux)

```bash
brew tap kivanccakmak/talos
brew install talcli                          # CLI
brew install --cask talos-label-printer      # desktop app
```

### Direct download

The latest release is always at
<https://github.com/kivanccakmak/talos-binaries/releases/latest> — direct asset
URLs follow this pattern:

```
https://github.com/kivanccakmak/talos-binaries/releases/latest/download/<asset-name>
```

For example:

```bash
# macOS arm64
curl -fsSL "https://github.com/kivanccakmak/talos-binaries/releases/latest/download/talcli-darwin-arm64" \
  -o /usr/local/bin/talcli && chmod +x /usr/local/bin/talcli
```

## Verifying downloads

Each release includes a `checksums.txt` with SHA-256 hashes:

```bash
shasum -a 256 -c checksums.txt
```

## Use with Claude Desktop

The Talos MCP server is also hosted at <https://mcp.talos.works/mcp> — add it
as a custom connector in Claude Desktop and you don't need to install anything
locally.

## License

Proprietary — Talos Works / SİMKAB. Binaries are provided for use with the
Talos platform only.
