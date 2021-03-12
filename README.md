# Codeup Setup Script

Setup script for Codeup students' laptops to install the all the tools we will
need for the java course. We will install the following:

- [xcode](https://developer.apple.com/xcode/features/): command line tools for
  macs
- [brew](http://brew.sh/): package manager for macs
- [java](https://en.wikipedia.org/wiki/Java_(programming_language))
- [tomcat](http://tomcat.apache.org/): the java webserver
- [maven](https://maven.apache.org/): a java dependency and build management tool
- [mysql](https://www.mysql.com/): the database we'll use for the class
- [node js](https://nodejs.org/en/): a JavaScript runtime outside the browser
- [npm](https://www.npmjs.com/): a package manager for JavaScript
- [intellij](https://www.jetbrains.com/idea/): a Java IDE

In addition, we will:

- setup ssh keys for the student's laptop and guide them through the process of
  linking their ssh key to their Github account.
- Setup a global gitignore file and set the default commit editor to `nano`
  (only if these are not already set)

## For Students

Copy and paste the following in your terminal:

```
bash -c "$(curl -sS https://raw.githubusercontent.com/gocodeup/codeup-setup-script/m1/install.sh)"
```

## Note for Instructors

If students already have and `id_rsa` ssh key generated the script will *not*
try to generate a new ones, and you will need to walk them through the process
of adding their existing key to Github.

The following should do the trick if they already have a ssh key pair, but it's
not wired up to Github.

```bash
pbcopy < ~/.ssh/id_rsa.pub
open https://github.com/settings/ssh
```
