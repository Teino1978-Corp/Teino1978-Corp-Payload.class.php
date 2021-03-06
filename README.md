# Teino1978-Corp-Payload.class.php
GitSharp /GitSharp/Remote.cs - https://searchcode.com/codesearch/view/7161954/

#RemoteCS#

#Convenient Coding Standards Validation for GitHub#

RemoteCS is a remote Coding Standard Validator for Github repositories. Unlike regular CS Validators, it doesn't requires any changes on the client side (no IDE plugin required neither pre-commit-hook setup for GIT). No need to set up on every developer's machine, just in one central place.

#Features:#

• RemoteCS is a GitHub WebHook - Activated after each commit

• Scans the newly added and the modified files after each commit (not the entire repository) on the committed branch

• Currently supports PHP: PHP lint for Syntax Checking and PHPCS for Coding Standards Validation

• Sends E-mail to the committer after commits about the results (if there is any result)

#Future directions:#

• Scan for ignore list file in each repository (example: /.remotecs-ignore)

• Send coding standard validation messages as inline comments into the commit to GitHub

• Multiple language support (Java, Ruby, Python, etc)

• Give points to the developers based on their code cleaniness & send weekly summary / toplist

• Web interface

#Prerequisites#

• PHP

• GIT

• PHPCS (PEAR/PHP_CodeSniffer)

• A webserver with sufficient rights to run all of the above

• Credentials for Amazon Simple Email Service to receive E-mails

#Quick Install#


• Copy the remotecs files to your webserver's directory

• Add the script's HTTP URL to Github -> Your Project -> Settings -> Service Hooks -> WebHook URLs

• Make sure the path's are correct in the Payload.class.php file & your webserver has sufficient rights

• Copy the config.sample.php into config.php and set up your Amazon Simple Email Service credentials to receive E-mails

• Press Test Hook or Commit & Push files

• If in trouble, enable debugging by $payload->debug(true); in index.php and check the debug.log file in the log directory

• Enjoy! =)

#References:#

PHP CodeSniffer: http://pear.php.net/package/PHP_CodeSniffer/

Author

Teino Boswell (teino@live.com)

Teino1978-Corp-index.html-codepen: https://github.com/Teino1978-Corp/Teino1978-Corp-index.html-codepen;

Github:  https://gist.github.com/Teino1978-Corp/forked 

