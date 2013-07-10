Stackato buildpack: Racket
==========================

This is a [Heroku-style buildpack](http://devcenter.heroku.com/articles/buildpacks) for Racket apps running on Stackato.
It uses [Racket](http://racket-lang.org).

Usage
-----

Example usage:

    $ ls
    stackato.yml web.mkt racketapp.mkt

    $ cat stackato.yml 
    ---
    name: racket
    framework:
      type: buildpack
    env:
      BUILDPACK_URL: git://github.com/philwhln/stackato-buildpack-racket.git
    processes:
      web: ./racketapp

    $ stackato push --no-prompt

The buildpack will detect that your app has a `racketapp.mkt` in the root.

