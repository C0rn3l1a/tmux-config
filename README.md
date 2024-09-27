# tmux-config
Install Tmux
```bash
brew install tmux
```

copy `.tmux.config` in your home dir (`~`)
```bash
curl https://raw.githubusercontent.com/C0rn3l1a/tmux-config/main/.tmux.conf > ~/.tmux.conf
```

install tpm 
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm

# type this in terminal if tmux is already running
tmux source ~/.tmux.conf
```

Then press [Ctrl] + [b] + [I] to install all plugins

and you should be good to go!

## Oh My Posh
Install Oh My Posh
```bash
brew install oh-my-posh
```

copy config
```bash
curl -s https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/main/themes/json.omp.json > ~/.my-posh.omp.json
```

then add to `~/.bashrc`
```bash
# Start tmux on startup
if command -v tmux &> /dev/null && [ -n "$PS1" ] && [[ ! "$TERM" =~ screen ]] && [[ ! "$TERM" =~ tmux ]] && [ -z "$TMUX" ]; then
  exec tmux
fi

eval "$(oh-my-posh init bash --config ~/.my-posh.omp.json)"
```
