# Fountain for Sublime Text #

This is an attempt to get the [Fountain](http://fountain.io) screenwriting syntax working in Sublime Text 2. This repo should work in TextMate as well, but the main testing is on Sublime Text 2 on a Mac.

Initial work on `Fountain.tmlanguage` created by Sublime Text forum use "nick" in [this post](http://www.sublimetext.com/forum/viewtopic.php?f=2&t=7442&p=31660).

## About Fountain ##

> Fountain is a simple markup syntax for writing, editing and sharing screenplays in plain, human-readable text. Fountain allows you to work on your screenplay anywhere, on any computer or tablet, using any software that edits text files.

Fountain is supported by a [growing list of apps](http://fountain.io/apps). Syntax highlighting is currently supported in Vim, TextWrangler and BBEdit. Brett Trepstra's [Marked](http://markedapp.com) can be [configured to work with Fountain](http://www.candlerblog.com/2012/02/08/fountain-for-marked/) files.

## Installation ##

### Method 1: Package Control ###

1. Install [Package Control](http://wbond.net/sublime_packages/package_control/installation).
2. Select `Package Control: Install Package` from the Command Palette (⇧⌘P).
3. Select Fountain.
4. Write the next *Full Metal Jacket*.

### Method 2: Download ###

1. Download and unzip this repo.
2. Zip the files inside the folder
3. Rename the zip to `Fountain.sublime-package` and move it to `~/Library/Application Support/Sublime Text 3/Installed Packages`.
4. Restart Sublime Text 3.
5. Write the next *Chinatown*.

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

Note that `Fountain.tmLanguage` supports much more of the syntax, but `Fountain Classic.tmTheme` only calls on the elements listed above using their custom scopes.

## Keyboard Shortcuts ##

There are a few included keyboard shortcuts to make writing your script easier.

* `*`, `**`, `(` and `[` - Wrap selected text with asterisks (single for italics, double for bold) parentheses or brackets as needed.
* `^⌘n` (control + command + n) - Note: If triggered with nothing selected will start a new Fountain formatted note (`[[This is a note.]]`). If triggered on selected text it will wrap it with double brakcets as a Fountain note.
* `^/` (control + /) - Boneyard: If triggered with nothing selected will start a new Fountain Boneyard section (`/*This is the boneyard*/`). If triggered on selected text it will wrap it in Boneyard formatting.

## Snippets ##

The current Fountain for Sublime Text package includes three snippets of varying usefulness. All are triggered from the Sublime Text's Command Pallette (⌘⇧P) by searching for them by name.

* **Title Page**: Creates a stock title page according to the Fountain syntax. Hitting `tab` after filling out each line will move the cursor to the following line.
* **Save the Cat**: An outline in Fountain format based on Blake Snyder's [book of the same name](http://amzn.to/UMpfWi).
* **int**: Creates an interior scene heading with the cursor placed just after "INT.". Pressing `tab` will move the cursor past the hyphen to fill out the scene's time (DAY, NIGHT, etc.). (Honestly you're better off just typing out your scene heading.)

## Customizations ##

The `Fountain.sublime-settings` files contains a number of customizations to make Sublime Text 2 a bit more writer friendly.

Currently it defaults to `Fountain Byworded Light.tmTheme` for syntax highlighting. This is a customized version of Philip Belesky's excellent ["Byworded" theme](https://github.com/philipbelesky/Byworded), itself based on the colors found in [Byword](http://bywordapp.com), a Mac OS X Text Editor. `Fountain Byworded Dark.tmtheme` is also included as a light on dark option.

The package also includes a custom version of the `Mac Classic` theme called `Fountain Classic.tmtheme` and Chris Kempson's Tomorrow night theme (`Fountain Tomorrow Night.tmtheme`).

In general Color Schemes will need to be customized with Fountain specific scopes. Use the provided themes as a guide for making your own.

## Help, Please ##

I spent about a day playing around with this to get the ball rolling, and I will continue fiddling with it. But if you know what's causing some of the current problems or ways to make this load cleaner, I'd appreciate it very much. Specifically, I'd like this to work with any color scheme, not customized ones. Also, if character and scene completions could be implemented, this would be a much better solution for nerdy screenwriters.

## Screenshot ##

![Sample Image][img]

[img]: http://f.cl.ly/items/272K2Z3l1m1V441c0p1b/Screen%20Shot%202012-11-16%20at%205.22.29%20PM.png

## Thanks ##

[John August](http://johnaugust.com/about) and [Stu Maschwitz](http://prolost.com/about/) jointly came up with Fountain and help maintain it. [Brett Terpstra](http://brettterpstra.com/about/)'s [MarkdownEditing](http://ttscoff.github.com/MarkdownEditing/) project served as the basis for how to customize ST2 for a specific syntax. And Brett's code for providing keyboard shortcuts to wrap code around text is used to wrap selected text in Notes and Boneyward blocks. [Oliver Taylor](http://olivertaylor.net)'s now deprecated Screenbundle TextMate Bundle was an inspiration for getting this off the ground.