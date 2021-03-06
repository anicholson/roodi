# 4.0.0
* Send args to roodi_task will make it easier to add custom configuration (breaking backwards compatibility)

# 3.3.1
* Not checking .erb files by default

# 3.3.0
* Using the roodi.yml in the current folder by default if it exists
* Added coloured output

# 3.2.0
* Checks all files under current directory by default
* Made it easier to run for the whole project as a rake task
* Added instructions for how to add Roodi to your Rakefile
* Removed support for Ruby Enterprise Edition
* Removed support for Ruby 1.8
* Improved installation instructions and corrected spelling error

# 3.1.1
* Merge pull request #23 from metricfu/remove_rubygems_require
  * Fix ruby warnings
  * Remove unnecessary require of rubygems

# 3.1.0
* Loosen ruby_parser version dependency (PR from Benjamin Fleischer)
* Files that can't be parsed are no longer silently skipped
* Empty rescue body check not failing when block contains empty arrays etc

# 3.0.1

* Added brief class level documentation on all checks
* No longer printing out "Line: 1" every time you run roodi-describe
* Added code coverage badge from Coverall.io
* Added code coverage through Coveralls.io
* Pulled duplicated find_name method up to super class
* Added Code Climate badge
* Added info about how to contribute
* Updated copyright info to be current
* Re-added tasks for releasing new versions of the gem

# 3.0.0

* Removed MissingForeignKeyIndexCheck, since it is specific to Rails/ActiveRecord and thus doesn't belong in Roodi
* A build is now running on Travis for the following Ruby versions: 1.8, 1.9, 2.0, JRuby 1.8 mode, JRuby 1.9 mode, Rubinius 1.8 mode, Rubinius 1.9 mode, Ruby Enterprise Edition
* Using ruby_parser 3.2.2
* Better check if OS is windows (#2 Martin Gotink)
* Accept 'next' in a rescue block (#1 Virgil Mihailovici)
* Rescue line count when there are no lines
* Pull down updates from https://github.com/zdennis/roodi that includes updates from https://github.com/hooroo/roodi and https://github.com/aselder/roodi re: pull request https://github.com/martinjandrews/roodi/pull/12 https://github.com/martinjandrews/roodi/pull/11

# 2.0.1

* Fixed a bug where roodi.yml was not being loaded.  Patch supplied by Rob Mitchell.

# 2.0.0

* Changed internal structure to use a more pure visitor like pattern.
* Got *much* faster as a result of the change.
* Design change fixed 'feature' where nested blocks would all get listed if the inner one exceeded complexity.
* Outline for NPath complexity check is now possible.  Not working yet though.
* Removed dependency on facets library.

# 1.4.0

* Upgraded from ParseTree to ruby_parser.

# 1.3.7

* Fixed a bug in the rake task where it always failed even if no errors existed.

# 1.3.6

* Added nil as a valid response for an empty rescue block

# 1.3.5

* Fixed bug in rake task

# 1.3.4

* Minor cleanup

# 1.3.3

* Added a rake task

# 1.3.1

* wrapped errors in an object to become more usable as an API.

# 1.3.0

* added case missing else check.
* updated checks to take a hash of options with built-in defaults.
* added support for complete configuration via external file.
* added support for passing in a custom config file via 'roodi -config=<filename> [pattern]'
* added assignment in conditional check.
* refactored checks to remove duplicate code.

# 1.2.0

* added module name check.
* added parameter number check.
* added module line count check.
* added class line count check.

# 1.1.1

* I'd initially published to Rubyforge under a 1.0.0 gem, and I've since tried to retrospectively fix up the version number system.  It turns out that Rubyforge caches old gems permanently, so I have to re-start at a larger number again.
* class name check no longer gets confused about scoped class names like Module::Classname.

# 0.5

* expanded regex matching for method name check.
* suppressed noisy output from ParseTree using facets API.
* updated dependencies and version as a result of facets change.
* made Roodi tolerant of being asked to parse files which aren't really Ruby files.
* updated the documentation with usage examples.

# 0.4

* Added support back in for line numbers in error messages.
* Re-enabled MethodLineCountCheck as part of the default check set.

# 0.3

* First version of Roodi to be published to Rubyforge.

# 0.2

* Now use ParseTree instead of JRuby, which makes the tool much more accessible.
* Removed MagicNumberCheck
* Line numbers no longer supported as a result of the move.

# 0.1

* A first version of a design checking tool for Ruby, with a few checks built in to get started.

