# MarketTime: Update Item Inventory



```
PUT https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/update-item-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MarketTime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/update-item-inventory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "string",
  "itemNumber": "string",
  "manufacturerId": "string",
  "name": "Ava Chen",
  "unitPrice": 1,
  "unitQuantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/update-item-inventory', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "string",
    "itemNumber": "string",
    "manufacturerId": "string",
    "name": "Ava Chen",
    "unitPrice": 1,
    "unitQuantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | string | yes |  |
| `useExternalId` | boolean | no |  |
| `recordId` | number | no | Required unless Use External ID is enabled. |
| `primaryImageUrl` | string | no | URL of primary image of item |
| `additionalImageUrl[]` | array<string> | no | List of URLs for additional images uploaded for items. Maximum of 6 allowed. |
| `caseQuantity` | number | no | Number of items available in a case |
| `catalogPageNumber` | number | no | Number of the catalog page where the item exists |
| `category` | string | no | Generic category name for the item |
| `dateIntroduced` | date | no | Date when the item was released |
| `defaultCancelDate` | date | no | Default cancel date for the item |
| `defaultShipDate` | date | no | Default shipping date for the item |
| `description` | string | no | Common description of item, can be longer than Name |
| `detailedDescription` | string | no | Additional description field |
| `discontinued` | string | no | Whether the item is discontinued |
| `discountEndDate` | date | no | Date at which a discount ends |
| `discountPercent` | number | no | Percentage of the item discount |
| `discountStartDate` | date | no | Date at which a discount begins |
| `hasImage` | string | no | Whether an image exists for the item |
| `isAvailable` | string | no | Whether the item is available |
| `commissionPercent` | number | no | Percentage of commission |
| `isCommissionable` | string | no | Whether the item is commissionable |
| `itemNumber` | string | yes |  |
| `itemID` | number | no | SKU, item number, or catalog number |
| `linkedItem` | string | no | Item connected to the added item |
| `manufacturerId` | string | yes |  |
| `minimumQuantity` | number | no | Minimum quantity for item. Required for create operations, but optional for this update operation. |
| `name` | string | yes |  |
| `nextAvailableDate` | date | no | Date at which the item is next available for order |
| `noFurtherDiscountApplied` | string | no | Whether further discount is applied to the item |
| `notes` | string | no | Custom notes for providing extra details |
| `quantityAvailable` | number | no |  |
| `quantityAvailableUpdated` | date | no |  |
| `qtyOnWater` | number | no | Current quantity for an item on water |
| `quantityIncrement` | number | no | Quantity increment for an item |
| `retailPrice` | number | no | Retail price for item, also known as MSRP |
| `season` | string | no | Item availability season |
| `showOnWebsite` | string | no | Whether to show this item on the website |
| `sizeUnitOfMeasure` | string | no | Unit of measure for the height, width, and length of the item |
| `tags` | string | no | Custom category names for item |
| `unitOfMeasure` | string | no | Unit of measure for the product |
| `unitPrice` | number | yes |  |
| `unitQuantity` | number | yes |  |
| `upc1` | string | no | UPC number for an item |
| `upc2` | string | no | Additional UPC number for an item |
| `upc3` | string | no | Additional UPC number for an item |
| `weight` | string | no | Weight of the product |
| `weightUnitOfMeasure` | string | no | Unit of measure for the product weight |
| `width` | string | no | Width of the product |
| `height` | string | no | Height of the product |
| `length` | string | no | Length of the product |
| `manufacturerCategory1` | string | no | First category of the manufacturer item |
| `manufacturerCategory2` | string | no | Second category of the manufacturer item |
| `manufacturerCategory3` | string | no | Third category of the manufacturer item |
| `categoryPath` | string | no | Concatenation of the manufacturer categories |
| `repGroupCategoryPath` | string | no | Concatenation of the RepGroup categories |
| `recordDeleted` | string | no | Whether the item record is deleted |
| `itemLineId` | number | no |  |
| `itemLineName` | string | no | Name of the item line |
| `externalId` | string | no | Value for referencing external systems |
| `externalId2` | string | no | Additional value for referencing external systems |
| `isPublic` | string | no |  |
| `isTopItem` | string | no |  |
| `sequencePublic` | number | no |  |
| `sequenceTopItem` | number | no |  |
| `manufacturerName` | string | no | Name of the manufacturer |
| `repGroupCategories[]` | array<object> | no |  |
| `scsDetails[]` | array<object> | no |  |
| `volumePricing[]` | array<object> | no |  |
| `dimensions` | string | no | Value of height, width, and length concatenated |
| `updatedFields` | string | no |  |
| `itemTag` | object | no |  |
| `keywords` | string | no |  |
| `newItem` | boolean | no |  |
| `updatedItem` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MarketTime API returns.

## Native endpoint

Through the native MarketTime API, this operation is `PUT /mtpublic/api/v1/:whoAmI/items/:whatItemDoIWantToUpdate` (base URL `https://publicapi.markettime.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item-inventory.md) for the provider-specific parameters and requirements.

