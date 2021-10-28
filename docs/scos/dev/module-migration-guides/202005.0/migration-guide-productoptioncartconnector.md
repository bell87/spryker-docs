---
title: Migration Guide - ProductOptionCartConnector
description: Use the guide to learn how to update the ProductOptionCartConnector module to a newer version.
last_updated: Sep 14, 2020
template: module-migration-guide-template
originalLink: https://documentation.spryker.com/v5/docs/mg-product-option-cart-connector
originalArticleId: 310276c4-7bf9-47a3-9685-ae2761606d48
redirect_from:
  - /v5/docs/mg-product-option-cart-connector
  - /v5/docs/en/mg-product-option-cart-connector
related:
  - title: Product Options
    link: docs/scos/user/back-office-user-guides/page.version/catalog/product-options/product-options.html
  - title: Migration Guide - Product Option
    link: docs/scos/dev/module-migration-guides/page.version/migration-guide-productoption.html
---

## Upgrading from Version 5.* to Version 7.0.0
{% info_block infoBox %}
In order to dismantle the Horizontal Barrier and enable partial module updates on projects, a Technical Release took place. Public API of source and target major versions are equal. No migration efforts are required. Please [contact us](https://spryker.com/en/support/) if you have any questions.
{% endinfo_block %}
## Upgrading from Version 4.* to Version 5.*

1. Update `spryker/product-option` to at least version 6.0.0. See [Migration Guide - Product Option](/docs/scos/dev/module-migration-guides/{{page.version}}/migration-guide-productoption.html).
2. Install/Update `spryker/price` to at least version 5.0.0. You can find additional information to price module upgrade: here.
3. Update `spryker/product-option-cart-connector` to version 5.0.0.
4. Optionally add `ProductOptionValuePriceExistsCartPreCheckPlugin` to your `CartPreCheckPlugin` list to pre-check product option value price if it exists before switching currency.
Example of plugin registration:
```php
<?php
namespace Pyz\Zed\Cart;

use Spryker\Zed\Cart\CartDependencyProvider as SprykerCartDependencyProvider;
use Spryker\Zed\Kernel\Container;
use Spryker\Zed\ProductOptionCartConnector\Communication\Plugin\ProductOptionValuePriceExistsCartPreCheckPlugin;

class CartDependencyProvider extends SprykerCartDependencyProvider
{
    /**
     * @param \Spryker\Zed\Kernel\Container $container
     *
     * @return \Spryker\Zed\Cart\Dependency\CartPreCheckPluginInterface[]
     */
    protected function getCartPreCheckPlugins(Container $container)
    {
        return [
            ...
            new ProductOptionValuePriceExistsCartPreCheckPlugin(),
            ...
        ];
    }
}
```

5. `ProductOptionCartConnectorToProductOptionInterface` was renamed to `ProductOptionCartConnectorToProductOptionFacadeInterface`. If you have implemented this interface, amend your implementation to use the new name.
6. Additional changes were made to `ProductOptionValueExpander` and to its factory method. Amend your code if you have customized or extended this class.

<!-- Last review date: Nov 10, 2017 by Karoly Gerner -->