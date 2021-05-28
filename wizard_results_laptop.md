Installation Wizard
Summary

    Xdebug installed: no
    Server API: Apache 2.0 Handler
    Windows: no
    Zend Server: no
    PHP Version: 7.4.7
    Zend API nr: 320190902
    PHP API nr: 20190902
    Debug Build: no
    Thread Safe Build: no
    OPcache Loaded: no
    Configuration File Path: /etc/php7/apache2
    Configuration File: /etc/php7/apache2/php.ini
    Extensions directory: /usr/lib64/php7/extensions

Instructions

    Download xdebug-3.0.4.tgz
    Install the pre-requisites for compiling PHP extensions. These packages are often called 'php-dev', or 'php-devel', 'automake' and 'autoconf'.
    Unpack the downloaded file with tar -xvzf xdebug-3.0.4.tgz
    Run: cd xdebug-3.0.4

    Run: phpize (See the FAQ if you don't have phpize).

    As part of its output it should show:

    Configuring for:
    ...
    Zend Module Api No:      20190902
    Zend Extension Api No:   320190902

    If it does not, you are using the wrong phpize. Please follow this FAQ entry and skip the next step.
    Run: ./configure
    Run: make
    Run: cp modules/xdebug.so /usr/lib64/php7/extensions
    Edit /etc/php7/apache2/php.ini and add the line
    zend_extension = /usr/lib64/php7/extensions/xdebug.so
    Please also update php.ini files in adjacent directories, as your system seems to be configured with a separate php.ini file for the web server and command line.
    Restart the webserver
