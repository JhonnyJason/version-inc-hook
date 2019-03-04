# version-inc-hook
Includes a Perl script to generally install git hooks + includes a pre-commit hook which increments a number in a version file.

## Usage

- copy the git-hooks directory into the root of your desired git repository
- add/adjust the hooks to fit your needs
- execute ./install-hooks.pl from within the git-hooks directory
- Now they are ready and shared to all other repositories when you add and commit them
- Tell your contributors to also install the hooks so they also become active on their local repository
- don't forget to add, commit and push your hooks ;-)

## version-inc
Here a simple pre-commit hook is available. What it does is follows:

- check if the file "version" exists in the root directory of your git repository
- if it does exist - read it - increment it and save it
- if it does not exist - create it - write 0 and save it

*At best make sure there are no conflicts with files named version in the root of your git repository!*

Now you don't have to manually adjust your version number - maybe you want to create more a complex number? Maybe extend the complexity to be more useful still quite general, give a pull request. Cool updates are:

- Using Semver
- Incrementing the specific numbers on messages inside the commit message - like "update-major", or "update-minor" 
