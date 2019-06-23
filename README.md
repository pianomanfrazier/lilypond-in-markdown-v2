# LilyPond in Markdown Version 2

The reason for version 2 is to cleanup tracking git dependencies. In order for netlify to build the project I commited the cached audio and svg files. This was cluttering up the git repo and unnecessary. The plan going forward is to not use netlify but something else like a direct deploy of the build to AWS or surge.sh.

## Initial Motivation

My previous way of blogging about music was too tedious. This is a proof of concept to show that LilyPond markup can be rendered to inline SVG for the web.

I wrote a blog post about what I did in version 1 [here](https://pianomanfrazier.com/post/lilypond-in-markdown).

## External Dependencies

- LilyPond
- Timidity
- ffmpeg

TODO: Make a docker container with all dependencies to build the site.

In order to build the project the LilyPond extension assumes that `lilypond` is available in your path. So you must first install [LilyPond](http://lilypond.org/download.html).

In order to produce audio from the generated midi from LilyPond you will need timidity. ffmpeg is used to generate various audio formats for browser support from the timidity output (flac).

