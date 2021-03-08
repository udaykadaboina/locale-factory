# Locale Factory

This repo acts like a submodule consisting of locale files.

# Architecture

<!-- image goes here! -->

# Usage

1. Add this as a submodule to container app using the following command:

    `✗ git submodule add https://github.com/udaykadaboina/locale-factory.git lib/globalization`

2. Change the default location at which your Rails app looks for the locale files

    ```
    # config/application.rb

    config.i18n.load_path += Dir[Rails.root.join('lib','globalization', 'locales', '*.{rb,yml}')]

    ```

## Updating/Adding new translated content.

1. Clone this repo in directory other than your container app.

    `$ git clone https://github.com/udaykadaboina/locale-factory.git`

2. Modify the specific locale files and push it to remote repo

    `$ git commit -am "added new translation strings"`
    `$ git push origin main`

3. Now that the repo has new translations, pull those into the container app.

    `$ git submodule update`

    Note: In order to check if there is an update in the locale-factory repo. You can run `$ git status` to know a brief display if there are any uncommitted changes from the submodule.







