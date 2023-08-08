AI shell script solutions right in your prompt.

![SVG screencast of aish in action](./screencast.svg)

`aish` is a single file shell script for getting one-liner solutions from AI right into your terminal where you need them.
It asks OpenAI for a one-liner solution to your problem, shows it to you, and inserts it into your history if you confirm.
Once it's in your history you can press "up" twice and then run or edit the solution as you like.

## Install

```bash
curl https://raw.githubusercontent.com/chr15m/aish/main/aish > ~/bin/aish && chmod 755 ~/bin/aish
```

Make sure you set the environment variable `OPENAI_API_KEY` to [your OpenAI API key](https://platform.openai.com/account/api-keys).

Then you can simply run `aish` to get started.

## Examples

Prefix these queries with `aish` in your terminal to try them out:

- which process is running on port 8000
- numeric for loop boilerplate going from 5 to 15
- restart openssh
- start a simple webserver using python3
- rename every file in ~/images from .jpg to .png
- print out the source of function __git_ps1
- delete all unused docker images
- concatenate two .mkv video files
- use ffmpeg to shrink an mp4 file's size
- use imagemagick change the white background in screenshot.png to transparent
