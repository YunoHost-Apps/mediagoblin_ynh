# GNU MediaGoblin for YunoHost

NOTWORKING

**CAUTION:** the application is currently not maintained anymore and the installation
seems to fail on recent YunoHost version (see [#8](https://github.com/jeromelebleu/mediagoblin_ynh/issues/8)
and [#9](https://github.com/jeromelebleu/mediagoblin_ynh/issues/9)). Feel free to contribute!

[MediaGoblin](http://mediagoblin.org/) is a free software media publishing platform
that anyone can run.

**Shipped version:** 0.9.0

## Features

The supported and activated Media types are:
  * **image**
  * **video**
  * **audio**
  * **pdf** - if you want support for converting libreoffice supported
    documents as well, you will have to install *unoconv* and *libreoffice*.

The transcoding is done in a separate thread thanks to Celery.

The authentication is transparently managed by SSOwat which is made
available in GNU MediaGoblin by the *ynhauth* beta plugin and some patches
to the source code.

It is also possible to enable registration using *basic_auth* plugin too which
will rely on the MediaGoblin internal authentication - and not YunoHost one.
Both authentication mechanism will be available in that case. Please note
that YunoHost users will have to log in through the SSO and not the MediaGoblin
login page.

## Installation

From the command-line:

    $ sudo yunohost app install https://github.com/jeromelebleu/mediagoblin_ynh

From the Web administration:
  * Go to *Applications*
  * Click on *Install*
  * Scroll to the bottom of the page and put https://github.com/jeromelebleu/mediagoblin_ynh
    under **Install custom app**

## TODO

* Add backup/restore scripts
