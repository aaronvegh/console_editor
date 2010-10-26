
# Console editor

Based almost entirely on interactive_editor, written by Jan Berkel. See [the original GitHub project](http://github.com/jberkel/interactive_editor) for details.

The only difference between this project and interactive\_editor is its behaviour: the original project is intended for use in irb, and eval()'s the contents of your editor upon exit. The purpose of console\_editor is to let console application users edit text files that are not intended for evaluation by the script.

## Usage

    $ gem install console_editor

Put the following in your console script:

    require 'rubygems'
    require 'console_editor'

Then, in your console application:

    > nano                       # (use nano w/ temp file)
    > nano 'filename.rb'         # (open filename.rb in nano)
    > ed                         # (use EDITOR env variable)
    > [emacs|vim|mvim|nano|mate] # (other editors)

When you exit the editor, your script can continue its execution.

To try it out without installing the gem:

    $ git clone git://github.com/aaronvegh/console_editor.git

Include the lib/console\_editor.rb file in your script.

## Disclaimer

This is a quick and dirty rip from the interactive\_editor gem, so any legacy code from that project is due only to my haste and ignorance. Cheers!