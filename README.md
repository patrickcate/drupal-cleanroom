# Drupal Cleanroom

Drupal 9 boilerplate repo to more easily setup environments for use with Composer, Lando, and VSCode.

Mainly used for testing modules, themes, patches.

## Installation

From the terminal:

1. Clone repo to new folder: `git clone git@github.com:patrickcate/drupal-cleanroom.git MY_FOLDER_NAME`
2. Move into the new directory: `cd MY_FOLDER_NAME`
3. Remove the git repo: `rm -rf .git`
   - Create a new git repo for the project with `git init` if needed.
4. Change the `APP_NAME_PLACEHOLDER` app name in `.lando.yml` to something more relevant.
   - Example: `printf '%s\n' ',s/APP_NAME_PLACEHOLDER/my-awesome-app/g' w q | ed .lando.yml`
5. Run `lando start`
6. Run `lando composer install`
7. Run `lando drush site:install --db-url=mysql://drupal9:drupal9@database/drupal9 --account-pass=admin`

## Run PHP Unit Tests

### With Xdebug

1. Start `PhpUnit` debugger in VSCode.
2. Run: `lando phpunitdebug web/PATH_TO_TEST_FILE.php`

### Without Xdebug

Run: `lando phpunit web/PATH_TO_TEST_FILE.php`

## Run Xdebug

Start `Listen for XDebug` debugger in VSCode.
