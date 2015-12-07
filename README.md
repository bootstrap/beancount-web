# beancount web

Web interface for [beancount](http://furius.ca/beancount/).

Built on [Flask](http://flask.pocoo.org/) it relies on an artificial API (`api.py`) that calls into beancount and returns Python-`dict`s for consumption by the web application. 

Many views are very buggy as this is just a quickly-hacked-together-version of what a new web interface for beancount might look like. Especially the filters (Year, Tag) are very buggy. 

This is mainly a proof-of-concept and playground for figuring out what a new web interface for beancount should look (and feel) like, and not if the (numerical) results themselves are correct or not. 

## Usage

Installation: `python setup.py install`

### beancount-web

1. Start beancount-web: `beancount-web /Volumes/Ledger/example.ledger` (substitute with the path to your own beancount-file) to run the included web server.
2. Point your browser at `http://localhost:5000` to view the web interface.

### beancount-urlscheme

1. Run `beancount-urlscheme register` to register the `beancount://` URL scheme on your system (currently only Mac OS is supported).
2. Restart your browsers to make them aware of the new URL scheme (not neccesary for Safari)
3. Run `beancount-urlscheme seteditor "/usr/local/bin/subl {filename}:{line}"` (substitute with your own editor-command) to set the command to be run when a `beancount://` URL is opened. You can use the `{filename}`- and `{line}`-variables.

---
**Caution**: This is far from finished. Consider it *alpha*-software. Contributions are very welcome :-)
