# talos-binaries

Public binary releases for the Talos platform.

This repo holds **release artifacts only** — source code lives on GitLab at
<https://gitlab.com/kivanccakmak/talos>.

## What's published here

| Component | Description | Platforms |
|---|---|---|
| `talcli_*.tar.gz` / `.zip` | Talos CLI + MCP server (Go) | darwin/linux/windows × arm64/amd64 |
| `talos-*.dmg` / `.exe` / `.AppImage` / `.deb` | Desktop app (Electron) — MCP installer, label printing, network discovery | macOS arm64, Windows x64, Linux x86_64 |
| `talos-mobile_*_android.apk` | Android build of the Talos mobile app | Android 8+ |

iOS builds are published to the App Store / TestFlight, not here.

## Quick install

### Homebrew (macOS / Linux)

```bash
brew tap kivanccakmak/talos
brew install talcli                # CLI
brew install --cask talos          # desktop app (macOS)
brew install talos                 # desktop app (Linux)
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
# talcli (macOS arm64)
curl -fsSL "https://github.com/kivanccakmak/talos-binaries/releases/latest/download/talcli_2.1.0_darwin-arm64.tar.gz" \
  | tar -xz && mv talcli-darwin-arm64 /usr/local/bin/talcli

# Desktop app (macOS arm64)
open "https://github.com/kivanccakmak/talos-binaries/releases/latest/download/talos-2.0.0-arm64.dmg"

# Android APK
open "https://github.com/kivanccakmak/talos-binaries/releases/latest/download/talos-mobile_1.9.27_android.apk"
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
