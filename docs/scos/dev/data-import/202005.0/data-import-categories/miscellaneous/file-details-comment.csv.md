---
title: File details- comment.csv
last_updated: Sep 14, 2020
template: data-import-template
originalLink: https://documentation.spryker.com/v5/docs/file-details-commentcsv
originalArticleId: 1facba35-37d7-420f-a9f2-fdb7a0bd3d91
redirect_from:
  - /v5/docs/file-details-commentcsv
  - /v5/docs/en/file-details-commentcsv
---

This article contains content of the **comment.csv** file to configure [Comment](/docs/scos/user/features/{{page.version}}/comments-feature-overview.html)  information on your Spryker Demo Shop.

## Import file parameters 
These are the header fields to be included in the .csv file:

| Field Name | Mandatory | Type | Other Requirements/Comments | Description |
| --- | --- | --- | --- | --- |
| **message_key** | No | String |N/A* | Identifier of the message with the comment. |
| **owner_type** | No | String |N/A | Owner type that issued the comment. |
| **owner_key** | No | String |N/A | Owner key identifier who issued the comment. |
| **customer_reference** | No | String |N/A |Reference of the customer.  |
| **message** | No | String |N/A |Message with the comment.  |
*N/A: Not applicable.

## Dependencies

This file has the following dependency:
*     [customer.csv](/docs/scos/dev/data-import/{{page.version}}/data-import-categories/commerce-setup/file-details-customer.csv.html)

## Import template file and content example
A template and an example of the *comment.csv*  file can be downloaded here:

| File | Description |
| --- | --- |
| [comment.csv template](https://spryker.s3.eu-central-1.amazonaws.com/docs/Developer+Guide/Back-End/Data+Manipulation/Data+Ingestion/Data+Import/Data+Import+Categories/Miscellaneous/Template+comment.csv) | Comment .csv template file (empty content, contains headers only). |
| [comment.csv](https://spryker.s3.eu-central-1.amazonaws.com/docs/Developer+Guide/Back-End/Data+Manipulation/Data+Ingestion/Data+Import/Data+Import+Categories/Miscellaneous/comment.csv) | Comment .csv file containing a Demo Shop data sample. |
