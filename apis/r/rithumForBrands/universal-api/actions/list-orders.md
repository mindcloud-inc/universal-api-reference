# Rithum for Brands: List Orders



```
GET https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-orders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profile` | list<number> | no |  |
| `siteName` | string | no |  |
| `dateModifiedAfter` | date | no |  |
| `dateModifiedBefore` | date | no |  |
| `filter` | string | no | Examples: ProfileID eq ProfileID PaymentStatus eq 'Cleared' CreatedDateUtc ge 2016-03-02 and CreatedDateUtc lt 2016-03-03 BuyerEmailAddress eq 'first.last@example.com' |
| `expand` | string | no | Examples: Items,Fulfillments Fulfillments($expand=Items) Items($expand=Adjustments),Fulfillments($expand=Items) (see https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=3fccd3491bd5d1d42d9eea40604bcb70) |
| `select` | string | no | Return only selected fields |
| `exported` | boolean | no | Example: `true/false`. |
| `orderBy` | string | no | orderBy |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aliasType": "string",
      "asin": {},
      "blockComment": {},
      "blockedDateUtc": {},
      "blockedFromAdvertisingDateUtc": {},
      "brand": "string",
      "bundleType": "string",
      "buyItNowPrice": 1,
      "classification": {},
      "condition": {},
      "copyToAliases": {},
      "copyToChildren": {},
      "cost": {},
      "createdDateUtc": "string",
      "description": {},
      "ean": {},
      "estimatedShippingCost": {},
      "flag": "string",
      "flagDescription": {},
      "harmonizedCode": {},
      "height": {},
      "id": 1,
      "infiniteQuantity": true,
      "isAvailableInStore": true,
      "isBlocked": true,
      "isBlockedFromAdvertising": true,
      "isbn": {},
      "isDisplayInStore": true,
      "isExternalQuantityBlocked": true,
      "isInRelationship": true,
      "isParent": true,
      "lastSaleDateUtc": {},
      "length": {},
      "manufacturer": "string",
      "margin": {},
      "maxPrice": {},
      "minPrice": {},
      "mpn": {},
      "multipackQuantity": {},
      "openAllocatedQuantity": 1,
      "openAllocatedQuantityPooled": 1,
      "parentProductID": {},
      "parentSku": {},
      "pendingCheckoutQuantity": 1,
      "pendingCheckoutQuantityPooled": 1,
      "pendingPaymentQuantity": 1,
      "pendingPaymentQuantityPooled": 1,
      "pendingShipmentQuantity": 1,
      "pendingShipmentQuantityPooled": 1,
      "productType": "string",
      "profileID": 1,
      "quantitySoldLast14Days": {},
      "quantitySoldLast30Days": {},
      "quantitySoldLast60Days": {},
      "quantitySoldLast7Days": {},
      "quantitySoldLast90Days": {},
      "quantityUpdateDateUtc": "string",
      "receivedDateUtc": {},
      "referenceProductID": {},
      "referenceSku": {},
      "relationshipName": {},
      "reservePrice": 1,
      "retailPrice": 1,
      "secondChancePrice": {},
      "shortDescription": {},
      "sku": "string",
      "startingPrice": 1,
      "storeDescription": {},
      "storePrice": 1,
      "storeTitle": {},
      "subtitle": "string",
      "supplierCode": {},
      "supplierName": {},
      "supplierPO": {},
      "taxProductCode": {},
      "title": "string",
      "totalAvailableQuantity": 1,
      "totalQuantity": 1,
      "totalQuantityPooled": 1,
      "upc": {},
      "updatedDateUtc": "string",
      "varyBy": {},
      "warehouseLocation": {},
      "warranty": {},
      "weight": {},
      "width": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aliasType` | string |  |
| `asin` | object |  |
| `blockComment` | object |  |
| `blockedDateUtc` | object |  |
| `blockedFromAdvertisingDateUtc` | object |  |
| `brand` | string |  |
| `bundleType` | string |  |
| `buyItNowPrice` | number |  |
| `classification` | object |  |
| `condition` | object |  |
| `copyToAliases` | object |  |
| `copyToChildren` | object |  |
| `cost` | object |  |
| `createdDateUtc` | string |  |
| `description` | object |  |
| `ean` | object |  |
| `estimatedShippingCost` | object |  |
| `flag` | string |  |
| `flagDescription` | object |  |
| `harmonizedCode` | object |  |
| `height` | object |  |
| `id` | number |  |
| `infiniteQuantity` | boolean |  |
| `isAvailableInStore` | boolean |  |
| `isBlocked` | boolean |  |
| `isBlockedFromAdvertising` | boolean |  |
| `isbn` | object |  |
| `isDisplayInStore` | boolean |  |
| `isExternalQuantityBlocked` | boolean |  |
| `isInRelationship` | boolean |  |
| `isParent` | boolean |  |
| `lastSaleDateUtc` | object |  |
| `length` | object |  |
| `manufacturer` | string |  |
| `margin` | object |  |
| `maxPrice` | object |  |
| `minPrice` | object |  |
| `mpn` | object |  |
| `multipackQuantity` | object |  |
| `openAllocatedQuantity` | number |  |
| `openAllocatedQuantityPooled` | number |  |
| `parentProductID` | object |  |
| `parentSku` | object |  |
| `pendingCheckoutQuantity` | number |  |
| `pendingCheckoutQuantityPooled` | number |  |
| `pendingPaymentQuantity` | number |  |
| `pendingPaymentQuantityPooled` | number |  |
| `pendingShipmentQuantity` | number |  |
| `pendingShipmentQuantityPooled` | number |  |
| `productType` | string |  |
| `profileID` | number |  |
| `quantitySoldLast14Days` | object |  |
| `quantitySoldLast30Days` | object |  |
| `quantitySoldLast60Days` | object |  |
| `quantitySoldLast7Days` | object |  |
| `quantitySoldLast90Days` | object |  |
| `quantityUpdateDateUtc` | string |  |
| `receivedDateUtc` | object |  |
| `referenceProductID` | object |  |
| `referenceSku` | object |  |
| `relationshipName` | object |  |
| `reservePrice` | number |  |
| `retailPrice` | number |  |
| `secondChancePrice` | object |  |
| `shortDescription` | object |  |
| `sku` | string |  |
| `startingPrice` | number |  |
| `storeDescription` | object |  |
| `storePrice` | number |  |
| `storeTitle` | object |  |
| `subtitle` | string |  |
| `supplierCode` | object |  |
| `supplierName` | object |  |
| `supplierPO` | object |  |
| `taxProductCode` | object |  |
| `title` | string |  |
| `totalAvailableQuantity` | number |  |
| `totalQuantity` | number |  |
| `totalQuantityPooled` | number |  |
| `upc` | object |  |
| `updatedDateUtc` | string |  |
| `varyBy` | object |  |
| `warehouseLocation` | object |  |
| `warranty` | object |  |
| `weight` | object |  |
| `width` | object |  |

## Native endpoint

Through the native Rithum for Brands API, this operation is `GET Orders` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

