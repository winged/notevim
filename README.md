Notevim - a shell wrapper for quick access to notes
===================================================

Notevim is a tiny little tool that helps you opening a gvim window with
your notes - or fetching it to your current workspace if it's already
open somewhere else.

The usual workflow would be to run `notevim --dmenu`, which gives you
a menu of all files in your notes directory. You can then select the
desired file, which will get opened (unless already open).

There's also support for embedding it into your openbox menu structure,
or working from commandline.


Commandline overview
--------------------

     
     notevim <filename>  - open file in note directory
     notevim --openbox   - Openbox pipe menu with the files in the note dir
     notevim --dmenu     - Show dmenu as a selector for the files
     notevim --list      - Normal list of the files in the note dir
     notevim             - Without any parameters, shows this help text


Openbox Menu entry
------------------

Use the following in your menu.xml to have a nice menu entry for your
notes:

    <menu execute="/PATH/TO/notevim --openbox" id="notes" label="Notes"/>

