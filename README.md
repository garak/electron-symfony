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
* put your Symfony project under `project` directory. If you prefer a different name, just edit `main.js` accordingly
* for portability, you should put a php static installation under `php` directory. If want to just give a try,
  you could use your already system-wide installed PHP. In this case, edit `main.js` and point the PHP path
  to your actual path (in the `bin` option of `php.server()`). E.g., for Ubuntu the path is `usr/bin/php`
* for portability, you should use a sqlite database. If you want to just give a try, you can use a "classic" database
  (like MySql)
* if your Symfony project is using assets from a CDN, you must copy such assets in your local folders, since
  CDN assets are not working inside electron.
  For example, if you're using something like `//code.jquery.com/jquery-2.2.3.js`, you need to
  downalod `jquery-2.2.3.js` file and put it under `web/js` directory, then adjust your templates accordingly.
* Also, if you use jquery, take a look to [this issue](http://stackoverflow.com/a/37480521/369194)

Execution
---------

Run `npm start`

The following screenshot shows an example of Symfony Standard Edition running with DevTools open:

![screenshot](https://cloud.githubusercontent.com/assets/179866/15629379/f3c89fca-2517-11e6-9455-9ba87abeba54.png)

If you want to use DevTools, uncomment the relevant line in `main.js`

