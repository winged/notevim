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


Openbox configuration
---------------------

Use the following in your menu.xml to have a nice menu entry for your
notes. This will give you a submenu for each of the files in your notes
directory.

    <menu execute="/PATH/TO/notevim --openbox" id="notes" label="Notes"/>

You can also add a shortcut to your openbox rc.xml to start it in dmenu mode.
In this example, if you press Windows-n, dmenu will start up with your notes to
choose from. This is what I'm using most of the time.

    <keybind key="W-n">
      <action name="Execute">
        <execute>notevim --dmenu</execute>
      </action>
    </keybind>


Sharing across different machines
---------------------------------

Okay, this is not built into the script, but I'm using SparkleShare
(http://sparkleshare.org/) to sync my notes to all my machines. 

Of course you could also use Dropbox, or a remotely mounted network share, or whatever.
