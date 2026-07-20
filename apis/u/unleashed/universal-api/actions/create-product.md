# Unleashed: Create Product

Creates a new product in Unleashed.

```
POST https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productCode": "string",
  "productDescription": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productCode": "string",
    "productDescription": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productCode` | string | yes | Unique code for the product. |
| `productDescription` | string | yes | Description for the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alternateUnitsOfMeasure": [
        {}
      ],
      "barcode": "string",
      "defaultPurchasePrice": 1,
      "defaultSellPrice": 1,
      "guid": "string",
      "imageUrl": "https://example.com",
      "inventoryDetails": [
        {}
      ],
      "isBatchTracked": true,
      "isPurchasable": true,
      "isSellable": true,
      "isSerialized": true,
      "lastCost": 1,
      "lastModifiedOn": "string",
      "notes": "string",
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
| `barcode` | string |  |
| `defaultPurchasePrice` | number |  |
| `defaultSellPrice` | number |  |
| `guid` | string |  |
| `imageUrl` | string |  |
| `inventoryDetails` | array<object> |  |
| `isBatchTracked` | boolean |  |
| `isPurchasable` | boolean |  |
| `isSellable` | boolean |  |
| `isSerialized` | boolean |  |
| `lastCost` | number |  |
| `lastModifiedOn` | string |  |
| `notes` | string |  |
| `obsolete` | boolean |  |
| `productCode` | string |  |
| `productDescription` | string |  |
| `productGroup` | object |  |
| `supplier` | object |  |
| `taxablePurchase` | boolean |  |
| `taxableSales` | boolean |  |
| `unitOfMeasure` | object |  |

## Native endpoint

Through the native Unleashed API, this operation is `POST /Products` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

