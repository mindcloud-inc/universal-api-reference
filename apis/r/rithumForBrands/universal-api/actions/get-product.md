# Rithum for Brands: Get Product



```
GET https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/get-product?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/get-product?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "context": "string"
      },
      "aliasType": "string",
      "asin": {},
      "blockComment": {},
      "blockedDateUtc": {},
      "blockedFromAdvertisingDateUtc": {},
      "brand": {},
      "bundleType": "string",
      "buyItNowPrice": {},
      "classification": {},
      "condition": {},
      "copyToAliases": {},
      "copyToChildren": {},
      "cost": {},
      "createDateUtc": "string",
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
      "manufacturer": {},
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
      "reservePrice": {},
      "retailPrice": {},
      "secondChancePrice": {},
      "shortDescription": {},
      "sku": "string",
      "startingPrice": {},
      "storeDescription": {},
      "storePrice": {},
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
      "updateDateUtc": "string",
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
| `@odata.context` | string |  |
| `aliasType` | string |  |
| `asin` | object |  |
| `blockComment` | object |  |
| `blockedDateUtc` | object |  |
| `blockedFromAdvertisingDateUtc` | object |  |
| `brand` | object |  |
| `bundleType` | string |  |
| `buyItNowPrice` | object |  |
| `classification` | object |  |
| `condition` | object |  |
| `copyToAliases` | object |  |
| `copyToChildren` | object |  |
| `cost` | object |  |
| `createDateUtc` | string |  |
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
| `manufacturer` | object |  |
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
| `reservePrice` | object |  |
| `retailPrice` | object |  |
| `secondChancePrice` | object |  |
| `shortDescription` | object |  |
| `sku` | string |  |
| `startingPrice` | object |  |
| `storeDescription` | object |  |
| `storePrice` | object |  |
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
| `updateDateUtc` | string |  |
| `varyBy` | object |  |
| `warehouseLocation` | object |  |
| `warranty` | object |  |
| `weight` | object |  |
| `width` | object |  |

## Native endpoint

Through the native Rithum for Brands API, this operation is `GET Products(:id)` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

