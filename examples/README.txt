This directory contains examples of using Ogre::BetaGUI.

To run the examples, you need to have OIS installed.

You also need three resource-related files:

1) plugins.cfg : this might be a symlink to a system-wide file,
for example on Ubuntu I did this:

  ln -s /etc/OGRE/plugins.cfg

2) resources.cfg : an example from OGRE 1.4.3 has been included
already. Be sure that the file paths point to where your media
files are; for example, I copy the OGRE Samples/Media/ files
into the examples directory like this:

  mkdir -p ogrenew-1.4.3/Samples/Media
  cp -r /tmp/ogrenew-1.4.3/Samples/Media/* ogrenew-1.4.3/Samples/Media/

and in resources.cfg all the entries look like this:

  Zip=ogrenew-1.4.3/Samples/Media/packs/skybox.zip

You can also use relative or absolute path names.
At the bottom of resources.cfg, add the following line:

  Zip=bguires.zip

This points to the resources file for BetaGUI that is included
in the Ogre::BetaGUI distribution in the examples directory.

3) bguires.zip : As just mentioned, this file contains
resources for BetaGUI, such as a .png file for the mouse pointer
and a material script file. You can modify these however you
want in order to customize your GUI. (In case I remove this file,
you might be able to find it at http://get.nxogre.org/betagui/
where I got it.)


Here are brief descriptions of the examples.
They are each put in a single file, though they would normally
be put in several files.

- itute2.pl : shows how to use a mouse cursor to place robots
  on a terrain; based on the Intermediate Tutorial 2 on the OGRE wiki
  (though that one uses CEGUI instead of BetaGUI).

- itute3.pl : place robots or ninjas on the terrain and also select
  and drag already-placed ones; ported from Intermediate Tutorial 3
  on the OGRE wiki (but again using BetaGUI in place of CEGUI)

- itute4.pl : drag a square to select groups of robots; ported from
  Intermediate Tutorial 4 on the OGRE wiki (but using BetaGUI)
