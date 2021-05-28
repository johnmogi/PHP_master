https://code.visualstudio.com/docs/languages/php

0. yarn init -y

0. package.json : 

{
  "name": "WWW", 
  "version": "1.0.0", 
  "main": "index.js", 
  "license": "MIT", 
  "dependencies": {}, 
  "devDependencies": {}, 
  "scripts": {

    "git": "git add . && git commit -m",
    "postgit": "git push --all"

  }
}

0. php debug - install ext

cd 	/etc/php7/apache2/php.ini
code / edit
zend_extension=path/to/xdebug

retry on normal with php server

paste phpinfo from php.ini >> 
https://xdebug.org/wizard
