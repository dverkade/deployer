<!-- DO NOT EDIT THIS FILE! -->
<!-- Instead edit recipe/pimcore.php -->
<!-- Then run bin/docgen -->

# How to Deploy a Pimcore Project

```php
require 'recipe/pimcore.php';
```

[Source](/recipe/pimcore.php)

Deployer is a free and open source deployment tool written in PHP. 
It helps you to deploy your Pimcore application to a server. 
It is very easy to use and has a lot of features. 

Three main features of Deployer are:
- **Provisioning** - provision your server for you.
- **Zero downtime deployment** - deploy your application without a downtime.
- **Rollbacks** - rollback your application to a previous version, if something goes wrong.

Additionally, Deployer has a lot of other features, like:
- **Easy to use** - Deployer is very easy to use. It has a simple and intuitive syntax.
- **Fast** - Deployer is very fast. It uses parallel connections to deploy your application.
- **Secure** - Deployer uses SSH to connect to your server.
- **Supports all major PHP frameworks** - Deployer supports all major PHP frameworks.

You can read more about Deployer in [Getting Started](/docs/getting-started.md).

The [deploy](#deploy) task of **Pimcore** consists of:
* [deploy:prepare](/docs/recipe/common.md#deployprepare) – Prepares a new release
  * [deploy:info](/docs/recipe/deploy/info.md#deployinfo) – Displays info about deployment
  * [deploy:setup](/docs/recipe/deploy/setup.md#deploysetup) – Prepares host for deploy
  * [deploy:lock](/docs/recipe/deploy/lock.md#deploylock) – Locks deploy
  * [deploy:release](/docs/recipe/deploy/release.md#deployrelease) – Prepares release
  * [deploy:update_code](/docs/recipe/deploy/update_code.md#deployupdate_code) – Updates code
  * [deploy:shared](/docs/recipe/deploy/shared.md#deployshared) – Creates symlinks for shared files and dirs
  * [deploy:writable](/docs/recipe/deploy/writable.md#deploywritable) – Makes writable dirs
* [deploy:vendors](/docs/recipe/deploy/vendors.md#deployvendors) – Installs vendors
* [deploy:cache:clear](/docs/recipe/symfony.md#deploycacheclear) – Clears cache
* [deploy:publish](/docs/recipe/common.md#deploypublish) – Publishes the release
  * [deploy:symlink](/docs/recipe/deploy/symlink.md#deploysymlink) – Creates symlink to release
  * [deploy:unlock](/docs/recipe/deploy/lock.md#deployunlock) – Unlocks deploy
  * [deploy:cleanup](/docs/recipe/deploy/cleanup.md#deploycleanup) – Cleanup old releases
  * [deploy:success](/docs/recipe/common.md#deploysuccess) – 


The pimcore recipe is based on the [symfony](/docs/recipe/symfony.md) recipe.


## Tasks

### pimcore:rebuild-classes
[Source](https://github.com/deployphp/deployer/blob/master/recipe/pimcore.php#L15)

Rebuilds Pimcore Classes.




### pimcore:custom-layouts-rebuild
[Source](https://github.com/deployphp/deployer/blob/master/recipe/pimcore.php#L20)

Creates Custom Layouts.




### pimcore:cache_clear
[Source](https://github.com/deployphp/deployer/blob/master/recipe/pimcore.php#L25)

Removes cache.




### pimcore:deploy
[Source](https://github.com/deployphp/deployer/blob/master/recipe/pimcore.php#L29)






This task is group task which contains next tasks:
* [pimcore:rebuild-classes](/docs/recipe/pimcore.md#pimcorerebuild-classes)
* [pimcore:custom-layouts-rebuild](/docs/recipe/pimcore.md#pimcorecustom-layouts-rebuild)

