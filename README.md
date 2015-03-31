Auto (Hard) Wrap for Sublime Text 2/3
====================
[![Build Status](https://travis-ci.org/randy3k/AutoWrap.svg?branch=master)](https://travis-ci.org/randy3k/AutoWrap)

Automatic hard wrap beyond wrap width.  It could be useful for text documents. [Sublime-Wrap-Plus](https://github.com/ehuss/Sublime-Wrap-Plus) could be used together with AutoWrap for the best experience.

![](https://raw.githubusercontent.com/randy3k/AutoWrap/master/screenshot.gif)

### Installation
[Package Control](http://wbond.net/sublime_packages/package_control)


### Usage

#### To toggle Auto Wrap
Type `Auto Wrap` in command palette or Go to menu `Edit -> Auto Wrap`.

#### Control wrap width

Wrap width is detected in the following order

1. `auto_wrap_width`
2. `wrap_width`
3. `rulers`
4. default 80

### Settings

#### To activate Auto Wrap for a specific syntax at start up

Put the following in your syntax specific preference.<br>
Menu -> Preference -> Settings - More -> Syntax Specific - User

    {
        "auto_wrap" : true
    }

#### You can also change `auto_wrap_width` by

    {
        "auto_wrap_width" : 100
    }

#### Long words

In default, long word will break into a new line.
To disable this behavior, consider

    {
        "auto_wrap_break_long_word" : false
    }

#### Break beyond wrap width only

If true, long sentence will break only if the cursor is beyond wrap width.

    {
        "auto_wrap_beyond_only" : true
    }

#### Break characters

It is an regular expression to define a set of characters for which a break would occur before them. (Backslash has to be double escaped.)

    {
        # it is the default
        "auto_wrap_break_chars" :  "[ ({\\[\\n]"
        # for latex, the following default is used
        # "auto_wrap_break_chars" : "\\\\left\\\\.|\\\\left.|\\\\\\{|[ ({\\[\\n]"
    }
