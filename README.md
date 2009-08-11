# Local Ports

I'm running MacPorts on my OS X box. These are some Portfiles I've
been adding to my system.

## Installation

    $ rake

This will generate the PortIndex, install a new MacPorts source
pointing at this directory, and set up a Git post-commit hook to
regenerate the PortIndex any time you commit Portfile changes.

Now you can `sudo port install guile19` and all sorts of goodies. For a
list of available local ports, try `rake list`. To manually update the
PortIndex (or to fix the Git hook, or the sources list), just run
`rake` again.

Fork and add your own.

(P.S. if you do fork, be sure to run `portindex` in the same directory
as this README.md when you change something. Alternatively, move
`git-hooks-pre-commit` to `.git/hooks/pre-commit` and make sure it's executable.)
