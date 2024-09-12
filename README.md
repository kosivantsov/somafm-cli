# Soma.FM bash/zsh cli interface

This is a simple shell script that defines two functions: `soma` and `soma64` with bash and zsh autocompletion for the available stations in the highest and 64-bit encoding, respectfully.
To make `soma` and `soma64` commands available, `somafmrc` available in this repo should be sourced from a file that is read by either bash or zsh (or both) when the shell is started. I use `$HOME/.aliases` for that by adding these lines (assuming `somafmrc` is located in `$HOME/.config/somafmrc`):
``` bash
if [ -f $HOME/.config/somafmrc ]; then
    source $HOME/.config/somafmrc
fi
```

Variable [`player`]([https://github.com/kosivantsov/somafm-cli/blob/7cb867bb5cc01d2044007c25ee720e9c15512555/somafmrc#L2) is set to `playurl`, another shell script that launches a user-defined player (including GUI players) and can get playable URLs for various resources, including YouTube video which will be played as audio-only.  
This variable can be set to any other player that accepts an URL as an argument.
