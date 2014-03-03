# MZ Box 
**A Phing Drupal boilerplate to kick-start Drupal development**

[![Build Status](https://travis-ci.org/marzeelabs/mz_box.png?branch=master)](https://travis-ci.org/marzeelabs/mz_box)

Boilerplate project to kick-start Drupal development using the excellent [Phing](http://www.phing.info) build system. For a general introduction to using Phing with Drupal, read our [blog post](http://marzeelabs.org/blog/2014/03/03/coding-as-a-team-automation-using-phing/).

### Getting started

Clone the repository and create the `build.properties` file.

	cp build.properties.example build.properties

Add your SQL database name, user and password in the file, and then

	phing make

to checkout all the required git repositories, and

	phing build

to install the site.

### Building your own makefile and installation profile

By default, this boilerplate will build the [MZ profile](https://github.com/marzeelabs/mz), which comes with makefiles that specify contributed modules and configuration we use our projects in [Marzee Labs](http://marzeelabs.org).

To build from your own makefile and installation profile, adapt the following settings and add to `build.properties`.

	drupal.make.repo = https://github.com/marzeelabs/mz
	drupal.make.makefile = build-mz.make
	drupal.make.revision = HEAD
	drupal.profile = mz

If you want to develop your profile, you can check out a working copy by setting
	
	drupal.make.working_copy = 1

If you have content fixtures using [Migrate](http://drupal.org/project/migrate) you can automatically migrate all of them during the build by setting
	
	drupal.migrate = 1

### Credits

Developed by [Marzee Labs](http://marzeelabs.org), [@marzeelabs](http://twitter.com/marzeelabs)
