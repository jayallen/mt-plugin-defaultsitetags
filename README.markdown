# DefaultSiteTags plugin for Movable Type v4 and Melody #

This is a very simple plugin which adds two template tags:

* `mt:SiteURL`
* `mt:SiteRoot``

These two tags correspond to the `DefaultSiteURL` and `DefaultSiteRoot` config directive settings in mt-config.cgi.

## VERSION ##

1.0 (released June 19th, 2009)

## REQUIREMENTS ##

* Movable Type 4.x or any version of Melody

## LICENSE ##

This program is distributed under the terms of the GNU General Public License,
version 2.

## INSTALLATION ##

Simply drop the directory `plugins/DefaultSiteTags` contained in this archive
into your `MT_HOME/plugins` directory.

If you are running under FastCGI or other persistent environment, you will
need to restart your webserver in order to activate the plugin in your Movable
Type installation.

## USAGE ##

In a typical setup when one blog publishes to the `DefaultSiteRoot` and others publish in subdirectories off of the root, `mt:BlogURL` is not predictable in global templates.  If all blogs share CSS, Javascript, a site images directory, etc, and you don't want to hardcode URLs, these two configuration directives are your salvation.

However, the only way to access these values is via the much longer:

    <$mt:Var name="config.DefaultSiteURL"$>
    <$mt:Var name="config.DefaultSiteRoot"$>

Ick.  Instead, we use:

    <$mt:SiteURL$>
    <$mt:SiteRoot$>

Much better...

## CONFIGURATION ##

The tags output the values of the `DefaultSiteURL` and `DefaultSiteRoot` configuration directives.  If these are not set, the tags output nothing.

## VERSION HISTORY ##

* 2009/06/19 - Initial release of v1.0

## SUPPORT ##

If you have additional feature requests or require support for an issue with
this plugin, please contact the author.

## AUTHOR ##

This plugin was brought to you by Jay Allen, Principal of Endevver Consulting
(http://endevver.com).

## COPYRIGHT ##

Copyright 2009, Endevver, LLC. All rights reserved.
