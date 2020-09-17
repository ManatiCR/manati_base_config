# Manatí Base Config Module [![Build Status](https://travis-ci.org/ManatiCR/manati-base-config.svg?branch=8.x)](https://travis-ci.org/ManatiCR/manati-base-config)

This module is used **only to import and enable custom config** of contrib modules used by Manatí. It should be used along with the [Bloom](https://github.com/ManatiCR/bloom) profile to import the first config of the new site.

## How to use it?

Install the drupal site using [Bloom](https://github.com/ManatiCR/bloom) installation profile.

Add the `manati_base_config` to your composer dependencies.

```php
composer require manaticr/manati_base_config
```

Enable the `manati_base_config` in order to enable all required modules. You could check all the required module dependencies at `/admin/modules` page.

```bash
drush en manati_base_config
```

Disable the `manati_base_config`.

```bash
drush pmu manati_base_config
```

Import the base config of the `manati_base_config` module.

```bash
drush cim --source=./modules/contrib/manati_base_config/config/partial --partial
```

Remove the module dependency from composer.

```php
 composer remove manaticr/manati_base_config
```

Enjoy the Manatí base config!!
