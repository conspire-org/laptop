Laptop
======

Laptop is a script to set up an OS X laptop for Rails development.
This is forked from Thoughtbot's Laptop script

Install
-------

Read, then run the script:

    bash <(curl -s https://raw.githubusercontent.com/stewartjarod/laptop/master/mac) 2>&1 | tee ~/laptop.log

Debugging
---------

Your last Laptop run will be saved to `~/laptop.log`. Read through it to see if
you can debug the issue yourself. If not, copy the lines where the script
failed into a [new GitHub
Issue](https://github.com/thoughtbot/laptop/issues/new) for us. Or, attach the
whole log file as an attachment.

What it sets up
---------------

* [Bundler] for managing Ruby libraries
* [Foreman] for serving Rails apps locally
* [Heroku Config] for local `ENV` variables
* [Heroku Toolbelt] for interacting with the Heroku API
* [Homebrew] for managing operating system libraries
* [ImageMagick] for cropping and resizing images
* [Node.js] and [NPM], for running apps and installing JavaScript packages
* [NVM] for managing versions of Node.js
* [Postgres] for storing relational data
* [Qt] for headless JavaScript testing via Capybara Webkit
* [RVM] for managing versions of Ruby
* [Redis] for storing key-value data
* [Ruby] stable for writing general-purpose code
* [Zsh] as your shell

[Bundler]: http://bundler.io/
[Foreman]: https://github.com/ddollar/foreman
[Heroku Config]: https://github.com/ddollar/heroku-config
[Heroku Toolbelt]: https://toolbelt.heroku.com/
[Homebrew]: http://brew.sh/
[ImageMagick]: http://www.imagemagick.org/
[Node.js]: http://nodejs.org/
[NPM]: https://www.npmjs.org/
[NVM]: https://github.com/creationix/nvm
[Postgres]: http://www.postgresql.org/
[Qt]: http://qt-project.org/
[Rails]: http://rubyonrails.org/
[RVM]: https://rvm.io/
[Redis]: http://redis.io/
[Ruby]: https://www.ruby-lang.org/en/
[Zsh]: http://www.zsh.org/

It should take less than 15 minutes to install (depends on your machine).

Laptop can be run multiple times on the same machine safely. It will upgrade
already installed packages and install and activate a new version of ruby (if
one is available).

Make your own customizations
----------------------------

Put your customizations in `~/.laptop.local`. For example, your
`~/.laptop.local` might look like this:

    #!/bin/sh

    brew tap caskroom/cask
    brew install brew-cask

    brew cask install dropbox
    brew cask install google-chrome
    brew cask install rdio

You should write your customizations such that they can be run safely more than
once. See the `mac` script for examples.

Credits
-------

![thoughtbot](http://thoughtbot.com/assets/tm/logo.png)

Laptop is maintained and funded by [thoughtbot, inc](http://thoughtbot.com/community).
The names and logos for thoughtbot are trademarks of thoughtbot, inc.

Thank you, [contributors](https://github.com/thoughtbot/laptop/graphs/contributors)!

Contributing
------------

Edit the `mac` file.

License
-------

Laptop is © 2011-2014 thoughtbot, inc. It is free software, and may be
redistributed under the terms specified in the LICENSE file.
