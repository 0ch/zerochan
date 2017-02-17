zerochan - A fork of lainchan
========================================================

About
------------
zerochan is a fork of [Lainchan](https://github.com/lainchan/lainchan), which is a fork of [vichan](http://github.com/vichan-devel/vichan). At the moment it's basically exactly the same.

Requirements
------------
1.	PHP >= 5.4 (we still try to keep compatibility with php 5.3 as much as possible)
        PHP 7.0 is explicitly supported.
2.	MySQL/MariaDB server
3.	[mbstring](http://www.php.net/manual/en/mbstring.installation.php) 
4.	[PHP GD](http://www.php.net/manual/en/intro.image.php)
5.	[PHP PDO](http://www.php.net/manual/en/intro.pdo.php)

We try to make sure zerochan is compatible with all major web servers and
operating systems. zerochan does not include an Apache ```.htaccess``` file nor does
it need one.

### Recommended
1.	MySQL/MariaDB server >= 5.5.3
2.	ImageMagick (command-line ImageMagick or GraphicsMagick preferred).
3.	[APC (Alternative PHP Cache)](http://php.net/manual/en/book.apc.php),
	[XCache](http://xcache.lighttpd.net/) or
	[Memcached](http://www.php.net/manual/en/intro.memcached.php)

Contributing
------------
You can contribute to zerochan by:
*	Developing patches/improvements/translations and using GitHub to submit pull requests
*	Providing feedback and suggestions
*	Writing/editing documentation
*	Fixing issues in the /0040/ sticky
* 	Adding requested features in the sticky

To do:
*	Add a wiki to make configuring and setting up the engine more documented
*	Fix banners
*	Fix auto-update
*	Fix image posting
*	Add user flags
*	Add wordfilters

Our IRC channel:

> irc.freenode.net @ ##0chan

Installation
-------------
1.	Download and extract zerochan to your web directory or get the latest
	development version with:

        git clone git://github.com/n1x3r/zerochan.git
	
2.	Navigate to ```install.php``` in your web browser and follow the
	prompts.
3.	zerochan should now be installed. Log in to ```mod.php``` with the
	default username and password combination: **admin / password**.

Please remember to change the administrator account password.

See also: ~~[Configuration Basics](http://tinyboard.org/docs/?p=Config).~~ jk dead link, vichan has basically no documentation

Upgrade
-------
To upgrade from any version of Tinyboard or vichan:

Either run ```git pull``` to update your files, if you used git, or
backup your ```inc/instance-config.php```, replace all your files in place
(don't remove boards etc.), then put ```inc/instance-config.php``` back and
finally run ```install.php```.

To migrate from a Kusaba X board, use http://github.com/vichan-devel/Tinyboard-Migration

Support
--------
If you find a bug, please report it.

If you need assistance with installing, configuring, or using lainchan, you may
find support from a variety of sources:

*	If you're unsure about how to enable or configure certain features, make
	sure you have read the comments in ```inc/config.php```.
*	You can join lainchan's IRC channel for support
	[irc.freenode.net #lainchan](irc://irc.freenode.net/lainchan)
*	You can also try our IRC channel 
	irc.freenode.net ##0chan

### Tinyboard support
vichan, and by extension lainchan and zerochan, is based on a Tinyboard, so both engines have very much in common.

Once again, vichan has little documentation out there. You won't have much luck finding support for it, or tinyboard for that matter.

CLI tools
-----------------
There are a few command line interface tools, based on Tinyboard-Tools. These need
to be launched from a Unix shell account (SSH, or something). They are located in a ```tools/```
directory.

You actually don't need these tools for your imageboard functioning, they are aimed
at the power users. You won't be able to run these from shared hosting accounts
(i.e. all free web servers).

Localisation
------------
Wanting to have zerochan in your language? You can contribute your translations to vichan at this URL:

~~https://www.transifex.com/projects/p/tinyboard-vichan-devel/~~ jk another dead link

Oekaki
------
zerochan makes use of [wPaint](https://github.com/websanova/wPaint) for oekaki. After you pull the repository, however, you will need to download wPaint separately using git's `submodule` feature. Use the following commands:

```
git submodule init
git submodule update
```

To enable oekaki, add all the scripts listed in `js/wpaint.js` to your `instance-config.php`.

WebM support
------------
Read `inc/lib/webm/README.md` for information about enabling webm.

lainchan API
----------
zerochan provides by default lainchan's 4chan-compatible JSON API, just like vichan. For documentation on this, see:
https://github.com/vichan-devel/vichan-API/ .

License
--------
See [LICENSE.md](http://github.com/n1x3r/zerochan/blob/master/LICENSE.md).

