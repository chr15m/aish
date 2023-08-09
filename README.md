Instant shell script solutions from AI right in your prompt.

![SVG screencast of aish in action](./screencast.svg)

`aish` is a single file shell script for getting one-liner solutions from AI right into your terminal where you need them.
It asks OpenAI for a one-liner solution to your problem, shows it to you, and inserts it into your history if you confirm.
Once it's in your history you can press "up" and then run or edit the one-liner as you like.

By default `aish` 

## Install

```bash
curl https://raw.githubusercontent.com/chr15m/aish/main/aish > ~/bin/aish && chmod 755 ~/bin/aish
```

Then you can simply run `aish` to get started:

```bash
. aish show me which process is running on port 8000
```

Make sure you set the environment variable `OPENAI_API_KEY` to [your OpenAI API key](https://platform.openai.com/account/api-keys).
You can add the key to `~/.aish` if it's not in your environment already. See the [configure](#configure) section below for details.

## Examples

Prefix these queries with `. aish` in your terminal to try them out:

- which process is running on port 8000
- numeric for loop boilerplate going from 5 to 15
- restart openssh
- start a simple webserver using python3
- rename every file in ./images from .jpg to .png
- resize all of images in ./images to a maximum of 100 pixels in any dimension
- create a small webserver with netcat
- get the ips that amazon.com resolves to and ping each one
- list all network interfaces and their ip addresses
- print out the source of function __git_ps1
- delete all unused docker images
- concatenate two .mkv video files
- use ffmpeg to shrink an mp4 file's size
- use imagemagick change the white background in screenshot.png to transparent

## Configure

You can create a file `~/.aish` that will be sourced by the script.
You can use this to override the defaults sent to the AI.

Here are some examples of configuration variables you can set:

```bash
# Set or override the OpenAI API key
OPENAI_API_KEY=...your key...
# Override the shell the AI will create solutions for
# (default is to autodetect whatever shell you are in)
AISH_SHELL="zsh"
# Override the OS the AI will create solutions for
# (default is to autodetect the OS you are using)
AISH_OS="Mac OSX"
# Override the ChatGPT model to use
AISH_MODEL="gpt-3.5-turbo-0301"
```
