# fish shell custom, minimal, bash-like theme configurations with default fish shell features (autosuggestions, Syntax highlighting with extensive error checking, searchable command history, etc...)

Installing && Customizing The Fish Shell Steps:

# Update Repo's
```console
$ sudo apt-get update
```

# Install Fish
```console
$ sudo apt install fish
```

# Set Fish Shell as default
```console
$ chsh -s $(which fish)
```

# Run Fish Shell
```console
$ fish
```

# Remove Greeting
```console
> set fish_greeting
```

# Install curl
```console
> sudo apt install curl
```

# Install git
```console
> sudo apt install git
```

# Install powerline fonts
```console
> sudo apt install fonts-powerline
```

# show full paths
```console
> set -U fish_prompt_pwd_dir_length 0
```

# Create an alias (example)
```console
> alias aliasname "actualcommand"
```

# Custom Prompt
```console
> sudo gedit ~/.config/fish/functions/fish_prompt.fish
```

# Inside fish_prompt.fish:
# for user (default bash theme):

```bash
function fish_prompt -d "Write out the prompt"
    printf (set_color green --bold)'%s@%s'(set_color normal)':%s%s%s$ ' $USER $hostname \
            (set_color blue --bold) (prompt_pwd) (set_color normal)
end
```

# for root (clean):
```bash
function fish_prompt -d "Write out the prompt"
    printf (set_color normal --bold)'%s@%s'(set_color normal)':%s%s%s# ' $USER $hostname \
                (set_color normal --bold) (prompt_pwd) (set_color normal)
end
```
# repeat again for every user you want to setup
