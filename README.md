
DakInfoScreenProject
====================

What?
-----

This is a symfony 2 project with the [DakInfoScreenBundle][dakInfoScreenBundle] pre-installed.

Setup
-----

Run

    git submodule init
    git submodule update

Run `php app/check.php` to make sure your php instaltion has all it requires.

Make sure the web-server has read-write access to app/cache and app/logs.

Copy `app/config/parameters.ini.dist` to `app/config/parameters.ini`. Edit it according to your database needs.

Then execute the following:

    php vendor/bundles/Sensio/Bundle/DistributionBundle/Resources/bin/build_bootstrap.php
    php app/console doctrine:schema:create
    php app/console doctrine:fixtures:load
    php app/console assets:install web/ --symlink

You should now be able to navigate to `http://localhost/path/to/infoscreen/`.
If you get error messages please use `http://localhost/path/to/infoscreen/app_dev.php`.

[dakInfoScreenBundle]: https://github.com/eoma/DakInfoScreenBundle
