Magento Composer Package
========================

This repository is a package to make [Magento](http://www.magentocommerce.com/) installable via  [Composer](http://getcomposer.org/).

Usage
-----

Supposing that you've Composer installed, to install Magento you can do:

	$ composer create-project webgriffe/magento my-new-project 1.7.0.2-dev
	
To know wich versions of Magento are available check available branches.

Magento project installer for Composer
--------------------------------------

This package comes with a [Magento Installer Composer's script](https://github.com/webgriffe/magento-installer) that installs Magento on the given database. You'll be required to insert the following installation parameters:

* `locale`: e.g. _en_US_
* `timezone`: e.g. _America/Los_Angeles_
* `default_currency`: e.g. _USD_
* `db_host`: e.g. _localhost_
* `db_name`: e.g. _magento_
* `db_user`: e.g. _root_, **this user must be granted to create the database**
* `db_pass`: e.g. _password_
* `url`: e.g. _http://magento.local/_, **remember the trailing slash**
* `admin_firstname`: e.g _John_
* `admin_lastname`: e.g _Doe_
* `admin_email`: e.g _john.doe@foo.it_
* `admin_username`: e.g _admin_
* `admin_password`: e.g. _password123_, **note that Magento requires that admin password contains letters and numbers**

These parameters will be stored in `var/install.yml` and the installer will use them to install Magento. If something goes wrong during the installation you can relaunch it through the command `composer run-script post-install-cmd`.

Magento module installer for Composer
-------------------------------------

This package comes with the [Magento module installer for Composer by Magento Hackathon](https://github.com/magento-hackathon/magento-composer-installer). If you want to install an extension you have only to add it to your Composer's dependencies and then execute the command `composer update vendor/my-brand-new-extension`. See the relative documentation for further informations.

For any suggestions or bug report, please use GitHub's issues section. Thank you!