Local Ports
=

I'm running MacPorts on my OS X box. These are some Portfiles I've
been adding to my system.

If you check this repo out as, say, `/Users/jmh/ports`, and you want
to add it to MacPorts you would just have to add the line

    file:///Users/jmh/ports/ [default]

to the the file `/opt/local/etc/macports/sources.conf`. This line
should go above the `rsync://` line already there. This allows you to
override ports in the remote repository with your local one.

And then you're done. Now you can `port install guile19` and all sorts
of goodies.

Fork and add your own.
