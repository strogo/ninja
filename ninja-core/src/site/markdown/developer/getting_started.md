How to contribute
=================

Great you want to contribute!
-----------------------------

Contributing to Ninja is really simple. Well. There are some rules that you should follow:

- Make sure your feature is well tested.
- Make sure your feature runs inside ninja-demo-application.
- Make sure your feature is well documented (Javadoc).
- Make sure there is a tutorial inside the website (ninja-core/src/site/markdown).
- Make sure you are following the code style below.

Then send us a pull request and you become a happy member of the Ninja family :)


Code style
----------

- Default Sun Java / Eclipse code style (a default config for eclipse can be found at the project root eclipse-ninja-format.xml.
- If you change only tiny things only reformat stuff you actually changed. Otherwise reviewing is really hard.
- We use spaces.
- All files are UTF-8.


Making a release
-----------------

Making a Ninja release
 
1) Preliminary

- update changelog.md
- Make sure the archetypes are up-to-date

2) Release to central maven repo

- mvn release:clean
- mvn release:prepare
- mvn release:perform
- Log into http://oss.sonatype.org and release the packages

3) publish website

- git checkout TAG
- cd ninja-core
- mvn site site:deploy

4) Add new version info to wikipedia:

- http://en.wikipedia.org/wiki/Comparison_of_web_application_frameworks
- http://en.wikipedia.org/wiki/Ninja_Web_Framework

And back to develop:

- git checkout develop
