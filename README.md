# Fountain for Sublime Text #

This is an attempt to get the [Fountain](http://fountain.io) screenwriting syntax working in Sublime Text 2. This repo should work in TextMate as well, but the main testing is on Sublime Text 2 on a Mac.

Initial work on `Fountain.tmlanguage` created by Sublime Text forum use "nick" in [this post](http://www.sublimetext.com/forum/viewtopic.php?f=2&t=7442&p=31660).

## About Fountain ##

> Fountain is a simple markup syntax for writing, editing and sharing screenplays in plain, human-readable text. Fountain allows you to work on your screenplay anywhere, on any computer or tablet, using any software that edits text files.

Fountain is supported by a [growing list of apps](http://fountain.io/apps). Syntax highlighting is currently supported in Vim, TextWrangler and BBEdit. Brett Trepstra's [Marked](http://markedapp.com) can be [configured to work with Fountain](http://www.candlerblog.com/2012/02/08/fountain-for-marked/) files.

## Installation ##

1. Download and unzip this repo.
2. Rename folder to `Fountain` and move to `~/Library/Application Support/Sublime Text 2/Packages`.
3. Restart Sublime Text 2.
4. Write the next *Chinatown*.

### Notes ###

* Feel free to delete the `img` folder and `README.md` once you're up and running.
* Alternatively, you could clone the repo to the same location listed above.

## What Does it Do? ##

Fountain for Sublime Text adds syntax highlighting when editing `.fountain` documents. Currently supported highlight elements:

* Title Page
* Scene Headings
* Characters
* Parentheticals
* Transitions

Note that `Fountain.tmlanguage` supports much more of the syntax, but `Fountain Classic.tmTheme` only calls on the elements listed above using their custom scopes.

## Customizations ##

The `Fountain.sublime-settings` files contains a number of customizations to make Sublime Text 2 a bit more writer friendly. It also defaults to using `Fountain Classic.tmTheme` for syntax highlighting. This is a take on the included `Mac Classic` theme but using Fountain specific scopes. This isn't the most elegant solution, but it works for now.

In general Color Schemes will need to be customized with Fountain specific scopes which is why I'm including this relatively bare theme.

## What Doesn't Work? ##

The Fountain syntax supports indentations, but this theme doesn't. If you, for example, tab indent characters and dialogue, they will not be highlighted. This has no effect when converting your document with other software, such as [Highland](http://quoteunquoteapps.com/highland/).

## Help, Please ##

I spent about a day playing around with this to get the ball rolling, and I will continue fiddling with it. But if you know what's causing some of the current problems or ways to make this load cleaner, I'd appreciate it very much. Specifically, I'd like this to work with any color scheme, not customized ones. Also, if character and scene completions could be implemented, this would be a much better solution for nerdy screenwriters.

## Screenshot ##

![Sample Image][img]

[img]: https://raw.github.com/poritsky/fountain-sublime-text/master/img/sample.jpg

## Thanks ##

[John August](http://johnaugust.com/about) and [Stu Maschwitz](http://prolost.com/about/) jointly came up with Fountain and help maintain it. [Brett Terpstra](http://brettterpstra.com/about/)'s [MarkdownEditing](http://ttscoff.github.com/MarkdownEditing/) project served as the basis for how to customize ST2 for a specific syntax. [Oliver Taylor](http://olivertaylor.net)'s now deprecated Screenbundle TextMate Bundle was an inspiration for getting this off the ground.























