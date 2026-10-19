# File App

File App edits documents, spreadsheets and diagrams in local projects.

[Download the latest release](https://github.com/AM1010101/file-app-releases/releases/latest).

## macOS

The signed and notarized app supports Apple Silicon Macs with macOS 13 or later.

```sh
brew install --cask AM1010101/tap/file-app
```

Alternatively, download the Mac zip and move File App.app to Applications.

## Linux

The Linux server opens File App in your browser. Archives include Node and production dependencies.

With Homebrew:

```sh
brew install AM1010101/tap/tree-server
tree-server serve /path/to/project
```

Without Homebrew, download and check the archive for your architecture. This example installs version 0.1.0 on x64:

```sh
curl -fLO https://github.com/AM1010101/file-app-releases/releases/download/v0.1.0/tree-server-0.1.0-linux-x64.tar.gz
curl -fLO https://github.com/AM1010101/file-app-releases/releases/download/v0.1.0/tree-server-0.1.0-linux-x64.tar.gz.sha256
sha256sum -c tree-server-0.1.0-linux-x64.tar.gz.sha256
tar -xzf tree-server-0.1.0-linux-x64.tar.gz
./tree-server-0.1.0-linux-x64/bin/tree-server serve /path/to/project
```

For ARM64, replace `linux-x64` with `linux-arm64` in these commands.

Open the localhost URL printed by the server. For a remote server, use an SSH tunnel to its localhost port.

## Updates

```sh
brew update
brew upgrade --cask AM1010101/tap/file-app
# Or, for the browser server:
brew upgrade AM1010101/tap/tree-server
```

The source repository is private. Downloads include the applicable license and dependency notices.
