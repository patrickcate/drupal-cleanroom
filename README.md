# Drupal Cleanroom

Drupal 9 boilerplate repo to more easily setup environments for use with Composer, Lando, and VSCode.

Mainly used for testing modules, themes, patches.

## Installation

1. Clone repo to new folder.
2. Change `drupal-cleanroom` Lando app name to something more relevant.
3. Run `lando start`
4. Run `lando composer install`
5. Run `lando drush site:install`

## Run PHP Unit Tests

### With Xdebug

1. Start `PhpUnit` debugger in VSCode.
2. Run: `lando phpunitdebug web/[PATH_TO_TEST_FILE].php`

### Without Xdebug

Run: `lando phpunit web/[PATH_TO_TEST_FILE].php`

## Run Xdebug

Start `Listen for XDebug` debugger in VSCode.
