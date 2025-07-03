# Ansible Playbooks

This repository contains my personal Ansible playbooks for setting up various tools and configurations.

## RUNME

```sh
ansible-playbook  ubt-wsl.yml --ask-become-pass
```

## Roles:
- `common`: Common system configurations.
- `nvm`: Node Version Manager installation.
- `uv`: UV tool installation.
- `x-cmd`: X-CMD tool installation.
- `gemini`: Google Gemini Python library installation.
- `ansible-lint`: Ansible Lint installation.
- `gemini-cli`: Gemini CLI installation.
- `conda`: Conda installation and setup for deep learning.
- `chezmoi`: Chezmoi dotfile manager installation.
- `zsh`: Installs and configures Zsh, including plugin management with Antidote and optional Powerlevel10k theme setup.