Adjustable lab bench power supply unit
======================================

Credits
-------

This PSU was designed by SonelecMusique, and was published at

 http://www.sonelec-musique.com/electronique_realisations_alim_ajust_009.html

My contributions are limited to:

* creating breadboard layout using Frizing
* adding 2 switches for ease of use
* adding a protection diode for safety in case of polarity inversion


The Fritzing file does not contain any PCB layout information yet.  It
was created with Fritzing 0.7.7.


Visualizing history diffs
-------------------------

Git can be told to extract the .fz file from the .fzz, which is a
standard zip file, so you can ask for text-level diffs in the saved
XML.  Note that as of v0.7.7, Fritzing does not seem to use a
deterministic element order when writing the file, or does superfluous
changes of some sort behind your back, and that the diffs thus
produced currently contain too much noise to be of any use.

These UNIX-based instructions should work for most UNIX versions,
possibly including MacOS-X.

Write this simple "fzz-to-fz" shell script somewhere and make it executable:

    #!/bin/sh
    unzip -ca "$1" "*.fz"

Tell git to use it on zipped Fritzing files:

    $ git config --global --replace-all --bool diff.zipped-fritzing.binary true
    $ git config --global --replace-all diff.zipped-fritzing.textconv '~/local/bin/fzz-to-fz'
