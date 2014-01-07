BcBootstrapBundle
=================

By [Florian Eckerstorfer](http://florianeckerstorfer.com)

[![Build Status](https://secure.travis-ci.org/braincrafted/bootstrap-bundle.png)](http://travis-ci.org/braincrafted/bootstrap-bundle)


About
-----

BcBootstrapBundle is [Bootstrap, from Twitter](http://twitter.github.com/bootstrap/) encapsulated in a [Symfony2](http://symfony.com) bundle.

This bundle is highly opiniated by how I use Twitter Bootstrap and Symfony.


Installation
------------

First you need to add `braincrafted/bootstrap-bundle` to `composer.json`:

    {
       "require": {
            "braincrafted/bootstrap-bundle": "dev-master"
        }
    }

Please note that `dev-master` points to the latest release. If you want to use the latest development version please use `dev-develop`. Of course you can also use an explicit version number, e.g., `1.4.*`.

You also have to add `BcBootstrapBundle` to your `AppKernel.php`:

    // app/AppKernel.php
    ...
    class AppKernel extends Kernel
    {
        ...
        public function registerBundles()
        {
            $bundles = array(
                ...
                new Bc\Bundle\BootstrapBundle\BcBootstrapBundle()
            );
            ...

            return $bundles;
        }
        ...
    }


Download Assets
---------------

This bundle does no longer contain the asset files from Twitter Bootstrap (images, stylesheets and JavaScripts). The best way to include those assets is to add Twitter Bootstrap to your `composer.json`:

    {
       "require": {
            "twbs/bootstrap": "2.3.*"
        }
    }

You can find a detailed description in the documentation.


More Information
----------------

Check out the [documentation](http://bootstrap.braincrafted.com) to find out how you can use BcBootstrapBundle in your Symfony2 project.


Compatibility
-------------

This bundle has two main dependencies, Symfony and Bootstrap. The following table shows which version of BraincraftedBootstrapBundle is compatible with which version of Symfony and Bootstrap.

<table>
    <thead>
        <tr>
            <th>BootstrapBundle</th>
            <th>Symfony</th>
            <th>Bootstrap</th>
            <th>jQuery</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>v1.3.*</strong></td>
            <td>v2.2.*</td>
            <td>v2.3.*</td>
            <td>v1.9.*</td>
        </tr>
        <tr>
            <td><strong> v1.4.*</strong></td>
            <td> `~2.3.0` (>=2.3.0,<2.4)</td>
            <td>v2.3.*</td>
            <td>v1.9.*</td>
        </tr>
        <tr>
            <td><strong>v1.5.*</strong></td>
            <td>v2.2.*</td>
            <td>v2.3.*</td>
            <td>v1.9.*</td>
        </tr>
        <tr>
            <td><strong>v2.0.*</strong></td>
            <td>v2.3.*<br>v2.4.*</td>
            <td>v3.0.*</td>
            <td>v1.10.*</td>
        </tr>
    </tbody>
</table>


Changelog
---------


### Version 1.4.0

- Extend from base form layout
- Allow override options in menus
- Fixed problems with removing elements in JavaScript collection form type
- Works with new Bootstrap repository `twbs/bootstrap`
- Changed namespace to `Bc\Bundle\BootstrapBundle`
- Automatically configure Twig
- Automatically configure KnpMenuBundle
- Automatically configure KnpPaginatorBundle
- Automatically configure Assetic
- Improved layout of error messages in compound fields
- Improved code style (usage of PHP_CodeSniffer and PHPMD)
- Support for `data-prototype` option in collection fields
- Helper and template for flash messages

License
-------

- The bundle is licensed under the [MIT License](http://opensource.org/licenses/MIT)
- The CSS and Javascript from the Twitter Bootstrap are licensed under the [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)
