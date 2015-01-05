# Midterms

Contained in this repository is my attempt to bring the power of open-souce to
my studying for my Junior year's midterms.  The process to generate these "study
guides" relies on LaTeX, and as such, generating PDFs is a bit convoluted.

## Setting Up

### Environment

First, you'll need to install a LaTeX environment on your computer.  If you're
running OSX, this is easy, just [install MacTeX](https://tug.org/mactex/).

### Packages

You'll then need a series of packages, each of which are used by documents in
this repository during processing.

Luckily, these packages are really easy to install once you have the MacTeX
environment on your system.  To install a package, simply run `tlmgr install
<package>` in your shell.

The necessary packages to process all the doucments are listed below:

- [mhchem](http://www.ctan.org/pkg/mhchem) - typeset chemical formulae/equations

## Compilation

PDF generation is done with [rubber](https://launchpad.net/rubber/), which can
be easily installed on OS X with homebrew.  To install, simply execute `brew
install rubber` in your shell.  Alternatively, you can download and compile the
source yourself, and then use `brew link` to link up the generated binaries in
your `bin/`.

To make all of this easy, there is a built in `rake` task that automates the
compilation of all `*.tex` files in each sub-directory.  That task is marked as
"default", so to run and compile, just hit `rake` in your shell.

## License

MIT
