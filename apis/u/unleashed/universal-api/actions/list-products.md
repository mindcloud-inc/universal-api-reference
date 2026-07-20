# Unleashed: List Products

Retrieves products from your Unleashed inventory catalog.

```
GET https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "alternateUnitsOfMeasure": [
        {}
      ],
      "averageLandPrice": 1,
      "copyCommentsForPurchases": true,
      "copyCommentsForSales": true,
      "createdBy": "string",
      "createdOn": "string",
      "defaultPurchasePrice": 1,
      "defaultPurchasesUnitOfMeasure": {},
      "defaultSellPrice": 1,
      "guid": "string",
      "inventoryDetails": [
        {}
      ],
      "isAssembledProduct": true,
      "isBatchTracked": true,
      "isComponent": true,
      "isPurchasable": true,
      "isSellable": true,
      "isSerialized": true,
      "lastCost": 1,
      "lastModifiedOn": "string",
      "maxStockAlertLevel": 1,
      "minStockAlertLevel": 1,
      "neverDiminishing": true,
      "obsolete": true,
      "productCode": "string",
      "productDescription": "string",
      "productGroup": {},
      "supplier": {},
      "taxablePurchase": true,
      "taxableSales": true,
      "unitOfMeasure": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alternateUnitsOfMeasure` | array<object> |  |
| `averageLandPrice` | number |  |
| `copyCommentsForPurchases` | boolean |  |
| `copyCommentsForSales` | boolean |  |
| `createdBy` | string |  |
| `createdOn` | string |  |
| `defaultPurchasePrice` | number |  |
| `defaultPurchasesUnitOfMeasure` | object |  |
| `defaultSellPrice` | number |  |
| `guid` | string |  |
| `inventoryDetails` | array<object> |  |
| `isAssembledProduct` | boolean |  |
| `isBatchTracked` | boolean |  |
| `isComponent` | boolean |  |
| `isPurchasable` | boolean |  |
| `isSellable` | boolean |  |
| `isSerialized` | boolean |  |
| `lastCost` | number |  |
| `lastModifiedOn` | string |  |
| `maxStockAlertLevel` | number |  |
| `minStockAlertLevel` | number |  |
| `neverDiminishing` | boolean |  |
| `obsolete` | boolean |  |
| `productCode` | string |  |
| `productDescription` | string |  |
| `productGroup` | object |  |
| `supplier` | object |  |
| `taxablePurchase` | boolean |  |
| `taxableSales` | boolean |  |
| `unitOfMeasure` | object |  |

## Native endpoint

Through the native Unleashed API, this operation is `GET /Products/:pageNumber` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

