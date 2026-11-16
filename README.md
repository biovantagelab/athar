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

## What's new in 0.0.23

- **Tokens for every round.** At the end of each round Athar shows the input,
  output and cached tokens it used, and thinking tokens where the provider
  reports them.
- **Subscription usage.** With a Claude or ChatGPT subscription, a line under
  the text box shows how much of each usage limit is used, for example
  `ChatGPT 30d 100%`, and says when credits pay past a full limit.
- **Sub-agents run together.** Several tasks handed to sub-agents in one step
  now run at the same time. A sub-agent can name its own model, and a project
  can save a default: `athar defaults --worker-provider P --worker-model M`.
- **Security fix.** A force push that nobody can be asked about now refuses,
  even after an earlier "yes" in the parent run.

Full notes: [release v0.0.23](https://github.com/biovantagelab/athar/releases/tag/v0.0.23).
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
athar --provider claude
```

Privacy Mode is off by default: when you choose a cloud model, Athar sends your
prompts and the files the agent reads to that provider. You are responsible for
that choice. To block the cloud, turn Privacy Mode on: `athar --privacy` for one
run, `athar defaults --privacy` for a project, or a local model in Ollama or LM
Studio. The `README.md` installed with Athar explains every model route,
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
