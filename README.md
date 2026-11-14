<p align="center">
  <a href="https://biovantagelab.com">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="assets/biovantagelab-logo-dark.svg">
      <img src="assets/biovantagelab-logo-light.svg" alt="BioVantageLab" height="64">
    </picture>
  </a>
</p>

# Athar

Athar is an AI research agent by [BioVantageLab](https://biovantagelab.com). It
runs in your terminal, works in your project folder, and helps you investigate
questions, examine evidence and build on earlier work.

Website: [biovantagelab.com](https://biovantagelab.com)

This is a **preview** for Macs (Apple Silicon or Intel) with macOS 13 or newer,
and for Linux (x86_64 or arm64, glibc 2.28 or newer, also Windows through WSL2).
It includes its own Python runtime, so you do not need Python, pip or
Homebrew. You do need a model provider: your own Claude Code sign-in, an OpenAI
API key, or a local model in Ollama or LM Studio.

## What's new in 0.0.20

- **Linux.** Athar now runs on Linux (x86_64 and arm64) and on Windows through
  WSL2. It runs every command in bubblewrap and gives it web access through
  pasta. Install them first (`sudo apt install bubblewrap passt` on Ubuntu and
  Debian); the install script names the command for your system. Ubuntu 24.04
  also needs an AppArmor profile: `athar doctor` names it. Publishing to GitHub
  does not work on Linux yet.
- **MCP servers.** `athar mcp add` adds a local server (npm, PyPI or an installed
  program) or a remote one (`--url`). Each local server runs in its own sandbox,
  and every call goes through Athar's permission check and privacy ledger.
  Privacy Mode refuses servers that use the network. `athar mcp test <name>`
  lists a server's tools.
- **ChatGPT.** Athar now reads the models your ChatGPT account can use, so it no
  longer fails with "model not supported".

Full notes: [release v0.0.20](https://github.com/biovantagelab/athar/releases/tag/v0.0.20).
If you have 0.0.3 or newer, run `athar update`.

## Install

Open Terminal and run:

```sh
curl -fsSL https://github.com/biovantagelab/athar/releases/latest/download/install.sh | sh
```

The script downloads the latest release, checks its SHA-256 checksum, and
installs Athar for your user only (`~/.local/bin/athar`). It stops and installs
nothing if the checksum does not match. To read the script first:

```sh
curl -fsSL https://github.com/biovantagelab/athar/releases/latest/download/install.sh | less
```

## Start

```sh
cd /path/to/your/project
athar doctor
athar --provider claude --allow-cloud
```

Privacy Mode is on by default: Athar sends nothing to a cloud provider until you
allow it. The `README.md` installed with Athar explains every model route,
updates and uninstalling. Its path is printed at the end of the install.

## Licence and responsibility

Athar is proprietary software from BioVantageLab. **It is not open source**, and
this repository holds no source code. Your use is governed by the
[Athar Preview Licence](LICENSE.md). Installing Athar means you accept it.

- You may use Athar for evaluation and your own research. You may not copy or
  pass on its files (sharing this page is fine), sell, modify or decompile it.
- Athar is an AI agent. It can run commands, change or delete files, and send
  your prompts and files to the model provider you choose. **You are fully
  responsible for what it does**, for checking its output, and for your backups.
- It gives no medical, clinical, legal, financial or safety advice.
- It comes with no warranty, and BioVantageLab is not liable for any loss or
  damage from its use.

## Contact

- Website: [biovantagelab.com](https://biovantagelab.com)
- Questions: melrefaiy@biovantagelab.com
