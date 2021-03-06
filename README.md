# DB Browser for SQLite

[![Build Status](https://travis-ci.org/sqlitebrowser/sqlitebrowser.svg?branch=master)](https://travis-ci.org/sqlitebrowser/sqlitebrowser)

![DB Browser for SQLite Screenshot](https://github.com/sqlitebrowser/sqlitebrowser/raw/master/images/sqlitebrowser.png "DB Browser for SQLite Screenshot")

## What it is

DB Browser for SQLite is a high quality, visual, open source tool to
create, design, and edit database files compatible with SQLite.

It is for users and developers wanting to create databases, search, and edit
data.  It uses a familiar spreadsheet-like interface, and you don't need to
learn complicated SQL commands.

Controls and wizards are available for users to:

* Create and compact database files
* Create, define, modify and delete tables
* Create, define and delete indexes
* Browse, edit, add and delete records
* Search records
* Import and export records as text
* Import and export tables from/to CSV files
* Import and export databases from/to SQL dump files
* Issue SQL queries and inspect the results
* Examine a log of all SQL commands issued by the application

## What it is not

This program is not a visual shell for the sqlite command line tool. It does
not require familiarity with SQL commands. It is a tool to be used both by
developers and by end users, and it must remain as simple to use as possible
in order to achieve its goals.

## What's been done since the SourceForge project

* Qt3Support was removed
* Recent files menu added
* Improved UI, making it more modern, replacing some dialogs etc.
* Syntax highlighting for SQL code
* Cleaned up the code, reducing the SLOC quite a bit
* Added basic support for triggers and views
* Added pragma editing
* Added BLOB support
* Added a new filter row for searching
* Improved performance when opening large tables
* Extended the SQL tab
* Added SQLite extension support
* Fixed a ton of bugs
* Probably more

All in all a fair amount of the code has been rewritten in order to regain
maintainability.  Based on this quite a few bugs can be fixed and new
features added.

## What's still to do

* Even more code cleanup
* Further improvement of the UI, adding more features and making it easier to use
* Feel free to add more issues at
  https://github.com/sqlitebrowser/sqlitebrowser/issues

## Windows binaries

Windows binaries can be downloaded from here:

* https://github.com/sqlitebrowser/sqlitebrowser/releases

Nightly builds are also available at:

* http://rp.oldsch00l.com/sqlitebrowser/

## MacOS X

DB Browser for SQLite works well on MacOS X.

* OSX 10.6 (Snow Leopard) - 10.9 (Mavericks) are tested and known to work

### MacOS X binaries

OSX binaries can be downloaded from here:

* https://github.com/sqlitebrowser/sqlitebrowser/releases

Nightly builds for OSX are available at:

* http://mirror.salasaga.org/sqlitebrowser/nightly/

### Compiling on MacOS X

The application can be compiled to a single executable binary file, similar to
other command line utilities.  Or it can be compiled to a .app bundle, suitable
for placing in /Applications.

### Compiling to a single executable binary

This is incredibly easy using [Homebrew](http://brew.sh).  Just run this command:

    $ brew install sqlitebrowser

And you're done.  A "sqlitebrowser" command should now be available in your PATH,
and can also be launched through Spotlight.

### Compiling to a .app bundle

Building the .app bundle version takes a bit more effort, but isn't too hard.
It requires SQLite and Qt 4.8.x to be installed first.  These are the
[Homebrew](http://brew.sh) steps, though other package managers should work:

    $ brew install sqlite --with-functions --without-readline
    $ brew install qt
    $ brew link sqlite3 --force

Then it's just a matter of getting the source:

    $ git clone https://github.com/sqlitebrowser/sqlitebrowser.git

**Note** - Don't clone the repo to a directory with a quote character (') in
it's name (eg ~/tmp/foo'), as compiling will error out.

And compiling it:

    $ cd sqlitebrowser
    $ qmake
    $ make
    $ brew unlink sqlite3
    $ mv src/sqlitebrowser.app /Applications/

An icon for "sqlitebrowser" should now be in your main OSX Applications
list, ready to launch.

## Twitter

Follow us on Twitter: https://twitter.com/sqlitebrowser

## Website

* http://sqlitebrowser.org

## Old project page

* https://sourceforge.net/projects/sqlitebrowser

## Releases

* [Version 3.3.1 released](https://github.com/sqlitebrowser/sqlitebrowser/releases/tag/v3.3.1) - 2014-08-31 - Project renamed from "SQLite Database Browser"
* [Version 3.3.0 released](https://github.com/sqlitebrowser/sqlitebrowser/releases/tag/v3.3.0) - 2014-08-24
* [Version 3.2.0 released](https://github.com/sqlitebrowser/sqlitebrowser/releases/tag/sqlb-3.2.0) - 2014-07-06
* [Version 3.1.0 released](https://github.com/sqlitebrowser/sqlitebrowser/releases/tag/sqlb-3.1.0) - 2014-05-17
* [Version 3.0.3 released](https://github.com/sqlitebrowser/sqlitebrowser/releases/tag/sqlb-3.0.3) - 2014-04-28
* [Version 3.0.2 released](https://github.com/sqlitebrowser/sqlitebrowser/releases/tag/sqlb-3.0.2) - 2014-02-12
* [Version 3.0.1 released](https://github.com/sqlitebrowser/sqlitebrowser/releases/tag/sqlb-3.0.1) - 2013-12-02
* [Version 3.0 released](https://github.com/sqlitebrowser/sqlitebrowser/releases/tag/sqlb-3.0) - 2013-09-15
* [Version 3.0rc1 released](https://github.com/sqlitebrowser/sqlitebrowser/releases/tag/rc1) - 2013-09-09 - Project now on GitHub
* Version 2.0b1 released - 2009-12-10 - Based on Qt4.6
* Version 1.2 released - 2005-04-05
* Version 1.1 released - 2004-07-20
* Version 1.01 released - 2003-10-02
* Version 1.0 released to public domain - 2003-08-19

## History

This program was developed originally by Mauricio Piacentini
([@piacentini](https://github.com/piacentini)) from Tabuleiro Producoes, as
the Arca Database Browser. The original version was used as a free companion
tool to the Arca Database Xtra, a commercial product that embeds SQLite
databases with some additional extensions to handle compressed and binary data.

The original code was trimmed and adjusted to be compatible with standard
SQLite 2.x databases. The resulting program was renamed SQLite Database
Browser, and released into the Public Domain by Mauricio. Icons were
contributed by [Raquel Ravanini](http://www.raquelravanini.com), also from
Tabuleiro. Jens Miltner ([@jmiltner](https://github.com/jmiltner)) contributed
the code to support SQLite 3.x databases for the 1.2 release.

Pete Morgan ([@daffodil](https://github.com/daffodil)) created an initial
project on GitHub with the code in 2012, where several contributors fixed and
improved pieces over the years. René Peinthor ([@rp-](https://github.com/rp-))
and Martin Kleusberg ([@MKleusberg](https://github.com/MKleusberg)) then
became involved, and have been the main driving force from that point.  Justin
Clift ([@justinclift](https://github.com/justinclift)) helps out with testing
on OSX, and started the new github.com/sqlitebrowser organisation on GitHub.

[John T. Haller](http://johnhaller.com), of
[PortableApps.com](http://portableapps.com) fame, created the new logo.  He
based it on the Tango icon set (public domain).

In August 2014, the project was renamed to "Database Browser for SQLite" at
the request of [Richard Hipp](http://www.hwaci.com/drh) (creator of
[SQLite](http://sqlite.org)), as the previous name was creating unintended
support issues.

In September 2014, the project was renamed to "DB Browser for SQLite", to
avoid confusion with an existing application called "Database Browser".

## License

DB Browser for SQLite is bi-licensed under the Mozilla Public License
Version 2, as well as the GNU General Public License Version 3 or later.

You can modify or redistribute it under the conditions of these licenses.
