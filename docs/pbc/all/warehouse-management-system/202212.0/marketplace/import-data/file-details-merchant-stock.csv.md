---
title: "File details: merchant_stock.csv"
last_updated: Feb 26, 2021
description: This document describes the merchant_stock.csv file to configure merchant stock information in your Spryker shop.
template: import-file-template
redirect_from:
  - /docs/marketplace/dev/data-import/202212.0/file-details-merchant-stock.csv.html
related:
  - title: Marketplace Merchant feature overview
    link: docs/pbc/all/merchant-management/page.version/marketplace/marketplace-merchant-feature-overview/marketplace-merchant-feature-overview.html
  - title: Execution order of data importers in Demo Shop
    link: docs/scos/dev/data-import/page.version/demo-shop-data-import/execution-order-of-data-importers-in-demo-shop.html
---

This document describes the `merchant_stock.csv` file to configure [merchant stock](/docs/pbc/all/warehouse-management-system/{{site.version}}/marketplace/install-features/install-the-marketplace-inventory-management-feature.html#marketplace-warehouse-management) information in your Spryker shop.


## Import file dependencies

<<<<<<<< HEAD:docs/pbc/all/warehouse-management-system/202212.0/marketplace/import-data/file-details-merchant-stock.csv.md
- [merchant.csv](/docs/marketplace/dev/data-import/{{site.version}}/file-details-merchant.csv.html)
- [warehouse.csv](/docs/pbc/all/warehouse-management-system/{{page.version}}/base-shop/import-data/file-details-warehouse.csv.html)
========
- [merchant.csv](/docs/pbc/all/merchant-management/{{site.version}}/marketplace/import-data/file-details-merchant.csv.html)
- [warehouse.csv](/docs/pbc/all/warehouse-management-system/{{page.version}}/import-and-export-data/file-details-warehouse.csv.html)


>>>>>>>> master:docs/pbc/all/merchant-management/202212.0/marketplace/import-data/file-details-merchant-stock.csv.md

## Import file parameters


| PARAMETER    | REQUIRED | TYPE | DEFAULT VALUE | REQUIREMENTS OR COMMENTS  | DESCRIPTION      |
| ------------- | -------- | ------ | ------------- | --------------------------------- | ----------------- |
| merchant_reference | &check;             | String   |                   | Unique                                                       | Identifier of the merchant in the system. |
| stock_name         | &check;             | String   |                   | Stock name is defined as described in [merchant warehouse](/docs/pbc/all/warehouse-management-system/{{site.version}}/marketplace/install-features/install-the-marketplace-inventory-management-feature.html#marketplace-warehouse-management). | Name of the stock.                        |


## Import template file and content example

| FILE  | DESCRIPTION    |
| --------------------- | --------------------- |
| [template_merchant_stock.csv](https://spryker.s3.eu-central-1.amazonaws.com/docs/Developer+Guide/Back-End/Data+Manipulation/Data+Ingestion/Data+Import/Data+Import+Categories/Marketplace+setup/template_merchant_stock.csv) | Import file template with headers only.         |
| [merchant_stock.csv](https://spryker.s3.eu-central-1.amazonaws.com/docs/Developer+Guide/Back-End/Data+Manipulation/Data+Ingestion/Data+Import/Data+Import+Categories/Marketplace+setup/merchant_stock.csv) | Example of the import file with Demo Shop data. |

## Import command

```bash
data:import merchant-stock
```