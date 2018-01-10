# teensy-tab-completion
tab completion for the teensy_loader_ci

At the moment there's a `zsh` completion file, others might be added in the future.

# USAGE

You might want to familiarize yourself with the `fpath` variable of the `zsh` completion system, e.g. in [this guide](https://github.com/zsh-users/zsh-completions/blob/master/zsh-completions-howto.org).

One way of using it: create the directory `${HOME}/.local/share/zsh/completions`, add it to `$fpath` and put `_teensy_loader_cli` there:

## Step1: In a shell
```sh
mkdir -p ${HOME}/.local/share/zsh/completions
cp _teensy_loader_cli ${HOME}/.local/share/zsh/completions
```

## Step2: Open `${HOME}/.zshrc` in an editor of your choice

add the line

```sh
fpath=(${HOME}/.local/share/zsh/completions $fpath)
```

somewhere before `autoload -Uz compinit; compinit`. (I guess this depends strongly on how your `.zshrc` is arranged).

## Step3: Start a new shell and enjoy

## comment

There may be better ways for future maintenance and pulling updates. Also you might already have custom completions or are looking for system wide installations, … or I might port the completion to other completion repositories. So be aware this is just one of many options of using the completion. Feel free to implement a better one.
