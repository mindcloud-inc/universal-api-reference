# Update Item Inventory with MarketTime

## Endpoint

- **Method:** `PUT`
- **Path:** `/mtpublic/api/v1/:whoAmI/items/:whatItemDoIWantToUpdate`
- **Base URL:** `https://publicapi.markettime.com`
- **Official documentation:** [Update Item Inventory](https://publicapi.markettime.com/swagger-ui/index.html#/Item/updateItem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whatItemDoIWantToUpdate` | path | `string` | yes | — |
| `useExternalID` | query | `boolean` | no | — |
| `recordID` | body | `number` | no | Required unless Use External ID is enabled. |
| `primaryImageUrl` | body | `string` | no | URL of primary image of item |
| `additionalImageUrl[]` | body | `array<string>` | no | List of URLs for additional images uploaded for items. Maximum of 6 allowed. |
| `caseQuantity` | body | `number` | no | Number of items available in a case |
| `catalogPageNumber` | body | `number` | no | Number of the catalog page where the item exists |
| `category` | body | `string` | no | Generic category name for the item Maximum length: 30. |
| `dateIntroduced` | body | `date` | no | Date when the item was released |
| `defaultCancelDate` | body | `date` | no | Default cancel date for the item |
| `defaultShipDate` | body | `date` | no | Default shipping date for the item |
| `description` | body | `string` | no | Common description of item, can be longer than Name Maximum length: 1000. |
| `detailedDescription` | body | `string` | no | Additional description field |
| `discontinued` | body | `string` | no | Whether the item is discontinued |
| `discountEndDate` | body | `date` | no | Date at which a discount ends |
| `discountPercent` | body | `number` | no | Percentage of the item discount |
| `discountStartDate` | body | `date` | no | Date at which a discount begins |
| `hasImage` | body | `string` | no | Whether an image exists for the item |
| `isAvailable` | body | `string` | no | Whether the item is available |
| `commissionPercent` | body | `number` | no | Percentage of commission |
| `isCommissionable` | body | `string` | no | Whether the item is commissionable |
| `itemNumber` | body | `string` | yes | Maximum length: 250. |
| `itemID` | body | `number` | no | SKU, item number, or catalog number |
| `linkedItem` | body | `string` | no | Item connected to the added item Maximum length: 50. |
| `manufacturerID` | body | `string` | yes | — |
| `minimumQuantity` | body | `number` | no | Minimum quantity for item. Required for create operations, but optional for this update operation. |
| `name` | body | `string` | yes | Maximum length: 50. |
| `nextAvailableDate` | body | `date` | no | Date at which the item is next available for order |
| `noFurtherDiscountApplied` | body | `string` | no | Whether further discount is applied to the item |
| `notes` | body | `string` | no | Custom notes for providing extra details Maximum length: 1000. |
| `qtyAvailable` | body | `number` | no | — |
| `qtyAvailableUpdated` | body | `date` | no | — |
| `qtyOnWater` | body | `number` | no | Current quantity for an item on water |
| `quantityIncrement` | body | `number` | no | Quantity increment for an item |
| `retailPrice` | body | `number` | no | Retail price for item, also known as MSRP |
| `season` | body | `string` | no | Item availability season Maximum length: 30. |
| `showOnWebsite` | body | `string` | no | Whether to show this item on the website |
| `sizeUnitOfMeasure` | body | `string` | no | Unit of measure for the height, width, and length of the item Maximum length: 45. |
| `tags` | body | `string` | no | Custom category names for item Maximum length: 250. |
| `unitOfMeasure` | body | `string` | no | Unit of measure for the product Maximum length: 25. |
| `unitPrice` | body | `number` | yes | — |
| `unitQty` | body | `number` | yes | — |
| `upc1` | body | `string` | no | UPC number for an item Maximum length: 30. |
| `upc2` | body | `string` | no | Additional UPC number for an item Maximum length: 30. |
| `upc3` | body | `string` | no | Additional UPC number for an item Maximum length: 30. |
| `weight` | body | `string` | no | Weight of the product Maximum length: 45. |
| `weightUnitOfMeasure` | body | `string` | no | Unit of measure for the product weight Maximum length: 45. |
| `width` | body | `string` | no | Width of the product Maximum length: 45. |
| `height` | body | `string` | no | Height of the product Maximum length: 45. |
| `length` | body | `string` | no | Length of the product Maximum length: 45. |
| `manufacturerCategory1` | body | `string` | no | First category of the manufacturer item Maximum length: 100. |
| `manufacturerCategory2` | body | `string` | no | Second category of the manufacturer item Maximum length: 100. |
| `manufacturerCategory3` | body | `string` | no | Third category of the manufacturer item Maximum length: 100. |
| `categoryPath` | body | `string` | no | Concatenation of the manufacturer categories |
| `repGroupCategoryPath` | body | `string` | no | Concatenation of the RepGroup categories |
| `recordDeleted` | body | `string` | no | Whether the item record is deleted |
| `itemLineID` | body | `number` | no | — |
| `itemLineName` | body | `string` | no | Name of the item line |
| `externalID` | body | `string` | no | Value for referencing external systems Maximum length: 50. |
| `externalID2` | body | `string` | no | Additional value for referencing external systems Maximum length: 100. |
| `isPublic` | body | `string` | no | — |
| `isTopItem` | body | `string` | no | — |
| `sequencePublic` | body | `number` | no | — |
| `sequenceTopItem` | body | `number` | no | — |
| `manufacturerName` | body | `string` | no | Name of the manufacturer |
| `repGroupCategories[]` | body | `array<object>` | no | — |
| `scsDetails[]` | body | `array<object>` | no | — |
| `volumePricing[]` | body | `array<object>` | no | — |
| `dimensions` | body | `string` | no | Value of height, width, and length concatenated |
| `updatedFields` | body | `string` | no | — |
| `itemTag` | body | `object` | no | — |
| `keywords` | body | `string` | no | — |
| `newItem` | body | `boolean` | no | — |
| `updatedItem` | body | `boolean` | no | — |
