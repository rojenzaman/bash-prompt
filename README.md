# bash-prompt
A lightweight (single file)  bash prompt.


## Features

* Single file installation to keep it simple
* Multiple color themes that can be switched in the same session
* Text input colorized to emphasize commands being executed
* Easy to modify contents of prompt

## Default Prompt

The included multi-line prompt has the following items:

* Time of day in HH:MM format
* Duration of previous command, colorized to indicate success or failure
* Username, colorized to indicate root or non-root user
* Hostname
* Current path trimmed to three directories (configurable)
* Current git branch if in a git repo
* Number of running/sleeping jobs

## Installation

Download [.bash_prompt](https://github.com/pkazmier/bash-prompt/blob/master/.bash_prompt)
to your $HOME directory. Select a theme from the list below or create your own. Then add
the following block of code to your `$HOME/.bashrc` or `$HOME/.bash_profile`, which will 
ensure the prompt is loaded only during an interactive session.

```bash
if [[ -n $PS1 && -f ~/.bash_prompt ]]; then
  . ~/.bash_prompt
  ps1_dark_theme  # Choose your theme here
fi
```
