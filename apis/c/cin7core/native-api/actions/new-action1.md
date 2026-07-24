# List Products with Cin7 Core

## Endpoint

- **Method:** `GET`
- **Path:** `product`
- **Base URL:** `https://inventory.dearsystems.com/externalapi/v2/`
- **Official documentation:** [List Products](https://dearinventory.docs.apiary.io/#reference/product/product/get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | query | `string` | no | Returns stock info of a particular product (Default: null) |
| `Name` | query | `string` | no | Only return products with product name containing specified name value (Default: null) |
| `Sku` | query | `string` | no | Only return products with product sku containing specified sku value (Default: null) |
| `ModifiedSince` | query | `date` | no | Only return Products modified since specified date (UTC time) in ISO 8601 format. (Default: null) |
| `IncludeDeprecated` | query | `boolean` | no | Returns all Products, including deprecated, if set to true. If set to false or if it is not specified then returns only active (ie. non-deprecated) Products (Default: false) |
| `IncludeBOM` | query | `boolean` | no | Include Bill Of Materials information (Default: false) |
| `IncludeSuppliers` | query | `boolean` | no | Include Suppliers information (Default: false) |
| `IncludeMovements` | query | `boolean` | no | Include Movements information (Default: false) |
| `IncludeAttachments` | query | `boolean` | no | Include Attachments information (Default: false) |
| `IncludeReorderLevels` | query | `boolean` | no | Include Reorder Levels information (Default: false) |
| `IncludeCustomPrices` | query | `boolean` | no | Include Customer specific Prices (Default: false) |
