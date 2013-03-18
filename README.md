BGWALL (bgwall) is a pipemenu generator for openbox.
It allows the changing of desktop wallpapers directly
from the openbox menu. Also, it uses perl. With that
said there are a few dependencies not everyone will
have installed by default.

DEPENDENCIES:
-------------

* PerlMagick
    * sudo apt-get install perlmagick
    * sudo cpan PerlMagick
    * http://www.imagemagick.org/script/perl-magick.php
    * http://search.cpan.org/dist/PerlMagick/
    * Or whatever is easier for you.

* feh
    * sudo apt-get install feh
    * http://feh.finalrewind.org/
    * Or whatever is easier for you.

INSTALLATION:
-------------

* From the terminal issue:
<pre>
    chmod +x bgwall
    sudo mv bgwall /usr/bin/bgwall
</pre>
* Then within your menu.xml add:
<pre>
    &ltmenu execute="bgwall" id="walls" label="walls"/&gt
</pre>

OTHER NOTES:
------------

- Usage of shred. I decided to go with shred for
  thumbnail removal basically on a whim. I fully know
  that "rm -rf" would have been much faster, and
  still went with "shred -f -u -z -n 1" if you want to
  change it to "rm -rf"... feel free to do so.

- At the end of the script you'll see that I forked the
  clean up subroutine. Let's be honest, every now and then
  you'll know you've made major changes to your wallpaper
  directory. This allows the script to be ran from terminal
  without a massive wait on when you have access to your
  prompt again. It would be good to note that if the
  switch is made to use "rm -rf", the fork would then not
  be necessary.
  
- LEGAL: This is open source. Feel free to change it 
  however you wish. Distribute it where ever you want. I 
  would however like credit. Also, I'm not responsible 
  for any damage caused to your computer due to any 
  changes you make.
