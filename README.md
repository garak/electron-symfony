Electron Symfony
================

This simple project allows to run a Symfony application inside Electron.
It's simply a default Electron build (see https://github.com/electron/electron-quick-start)
with gulp-connect-php, needed to run PHP.
Indeed, you can use this to run any PHP application, not just a Symfony one.

You need npm installed on your machine to get this working.

Installation
------------

* clone this repository
* run `npm install`
* put your Symfony project under `project` directory. If, for example, your project is
  named `myProject`, put it under `project/myProject`
* for portability, you should put a php static installation under `php` directory. If want to just give a try,
  you could use your already system-wide installed PHP. In this case, edit `main.js` and point the PHP path
  to your actual path. E.g., for Ubuntu the path is `usr/bin/php`
* for portability, you should use a sqlite database. If you want to just give a try and use a "classic" database
  (like MySql)
* if your Symfony project is using assets from a CDN, you must copy such assets in your local folders, since
  CDN assets are not working inside electron.
  For example, if you're using something like `//code.jquery.com/jquery-2.2.3.js`, you need to
  downalod `jquery-2.2.3.js` file and put it under `web/js` directory, then adjust your templates accordingly.

Execution
---------

Run `npm start`
