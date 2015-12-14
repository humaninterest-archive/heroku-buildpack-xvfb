# heroku-buildpack-xvfb

With [heroku-buildpack-apt](https://github.com/ddollar/heroku-buildpack-apt), this buildpack enables running

    xvfb-run program

on Heroku. To use it, ensure that `heroku-buildpack-apt` comes earlier than this in the buildpacks list, and include

    xvfb

in your `Aptfile`.

Some inspiration (for dealing with Xvfb's compiled-in `XKB_BIN_DIRECTORY`, which leads to it complaining that it can't find `/usr/bin/xkbcomp`) comes from fxtentacle's answer to http://stackoverflow.com/a/34219781/1162903.
