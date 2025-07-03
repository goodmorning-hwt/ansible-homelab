# ZSH Role

This Ansible role installs and configures Zsh with the Antidote plugin manager using a modular configuration approach.

## Features

- Installs Zsh shell
- Installs Antidote plugin manager
- Modular configuration structure for easy customization
- Sets up essential Zsh plugins including:
  - zsh-syntax-highlighting
  - zsh-autosuggestions
  - zsh-completions
  - zsh-history-substring-search
  - Git integration plugins
  - Colored man pages
  - Command not found suggestions
  - Spaceship prompt theme
  - fzf-tab for enhanced tab completion
  - And more useful plugins

## Configuration Structure

The role creates a modular configuration structure:

```
~/.zshrc                    # Main configuration file
~/.config/zsh/
├── history.zsh            # History settings and options
├── completion.zsh         # Completion configuration and styling
├── environment.zsh        # Environment variables and PATH
├── aliases.zsh            # Command aliases
└── spaceship.zsh          # Spaceship prompt configuration
```

## What it does

1. Installs Zsh package
2. Clones Antidote repository to `~/.antidote`
3. Creates `~/.config/zsh/` directory for modular configuration
4. Creates main `.zshrc` that loads modular configuration files
5. Creates modular configuration files for different aspects:
   - **history.zsh**: History file settings, size, and behavior options
   - **completion.zsh**: Advanced completion configuration with styling
   - **environment.zsh**: Environment variables, PATH modifications, and tool settings
   - **aliases.zsh**: Comprehensive set of useful aliases
   - **spaceship.zsh**: Detailed Spaceship prompt configuration
6. Creates `.zsh_plugins.txt` with curated plugin list
7. Changes default shell to Zsh
8. Verifies installation

## Customization

The modular structure makes it easy to customize:

- **Add custom aliases**: Edit `~/.config/zsh/aliases.zsh`
- **Modify prompt**: Edit `~/.config/zsh/spaceship.zsh`
- **Adjust history**: Edit `~/.config/zsh/history.zsh`
- **Change environment**: Edit `~/.config/zsh/environment.zsh`
- **Override settings**: Create `~/.zshrc.local` for local customizations

## Requirements

- Git (for cloning Antidote and plugins)
- Internet connection (for downloading plugins)

## Usage

The role is included in the main playbook and will be executed when running:

```bash
ansible-playbook -i inventory.ini ubt-wsl.yml
```

After installation, restart your terminal or run `exec zsh` to start using Zsh with the modular configuration.
