# Manatí Base Config Module

This module is used **only to import and enable the config** from the contrib modules used by Manatí. This module should be used along with the [Bloom](https://github.com/ManatiCR/bloom) profile.

## How to use it?

Install the drupal site using [Bloom](https://github.com/ManatiCR/bloom) installation profile.

Add the `manati_base_config` to your composer dependencies.

```bash
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
