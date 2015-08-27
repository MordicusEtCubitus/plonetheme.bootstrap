Fork notes
==========
This product is a fork of the great theme
https://github.com/collective/plonetheme.bootstrap, Master branch, 2015-08-27.

The fork as been done to:
    - Complete this great plonetheme for Plone 4 using latest bootstrap and 
      jQuery librairies
    - Remove all jquery, jquerytools, collective.js.bootstrap and others
      packages dependencies
      I really hate to have a package broken in many sub packages depencies,
      especially for a graphical theme. It should provide by itself all files 
      it needs, especially Javascript, CSS, images: this is the purpose of a 
      theme and my point of view.
      To put it in others words, I think that a theme *SHOULD NOT* be broken into
      many sub products as it counts CSS or JS files ! 
      This is too much complicated, difficult to maintain, provides an explosion
      of installed packages with only 2 js/css files fighting alone against the
      darkness and when it is broken because a dependency has been updated to a 
      new version, it is difficult to debug, because you don't know what people
      do with dependencies you need.
    - The package also desactivate all Plone CSS and JS in a default installation.
      I also think there are too too too much JS and CSS badly integrated
      into the default Plone installation. I hate this for so long.
      More, most of them are not really usable with Twitter Bootstrap.
      So, it is time to do a big cleanup in this ocean of everything 
      hurted in hurricane.
      It was time to change this; even if Plone 5 did it well I still working
      a lot on Plone 4 sites, and there are many for maintenance in the World.
    - This is a default theme no more relying on Sunburst
    - It also updates the main template to use Boostrap navbar
    - Removes others items
    - Add others stuffs...
    
This still in progress, but should move quite quickly as I need it actually 
in production environment as far as possible.

It is not ready yet, so don't expect too much now.
Will also move on Bootstrap 4 as soon as it will be released as an
official version.
      
      

Introduction
============

plonetheme.bootstrap integrates Twitter Bootstrap CSS/JS framework
into Plone. You can checkout the framework at http://getbootstrap.com/

It overrides some templates and uses javascript to transform
some markup in order for it to work correctly.

It's not perfect, but it's close.

.. image:: https://api.travis-ci.org/collective/plonetheme.bootstrap.png?branch=master
    :target: http://travis-ci.org/collective/plonetheme.bootstrap

Dependencies
==============



Documentation
===============

This product is based in Twitter Bootstrap version 3. 
The product no more reuse
`collective.js.bootstrap`_ to get those CSS and JS files and provides its owns.

The basic HTML markup is no more a mix of `plonetheme.sunburst`_ but only of
Twitter Bootstrap
and it uses the same approach of constructing the columns as Sunburst Theme:
a simple view that returns the classes needed to have the correct column widths.

If you want to change those widths, just override the view following the common
Plone overriding patterns.

This product is intended to be used in two scenarios:

 - As a theme from Plone
 - As a base theme to build Plone themes for your site following 'old practices'

Some designers prefer to work following the old best-practices instead of using
the Diazo-way-of-theming, this product is for them. You can create a theme package
(check `templer skeleton generator`_), and base your theme on this one.

If you have any problem using this product or find any bug, please report it
using the `GitHub issue tracker`_.

Upgrade
=========

To upgrade from version 1.0a1, just go to the add-on controlpanel and click
on upgrade. Old skin paths and javascripts will be disabled and new ones imported



Authors
=========

- Nathan van Gheem, initial author
- Mikel Larreategi, update to Twitter Bootstrap 2.3.x, current mantainer


.. _`templer skeleton generator`: http://templer-manual.readthedocs.org/en/latest/
.. _`GitHub issue tracker`: https://github.com/collective/plonetheme.bootstrap/issues
