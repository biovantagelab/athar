# Athar

Athar is an AI research agent by BioVantageLab. It runs in your terminal, works
in your project folder, and helps you investigate questions, examine evidence
and build on earlier work.

This is a **preview** for Apple Silicon Macs (M1 or later) with macOS 13 or
newer. It includes its own Python runtime, so you do not need Python, pip or
Homebrew. You do need a model provider: your own Claude Code sign-in, an OpenAI
API key, or a local model in Ollama or LM Studio.

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

Questions: melrefaiy@biovantagelab.com
