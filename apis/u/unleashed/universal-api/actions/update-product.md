# Unleashed: Update Product

Updates an existing product in Unleashed.

```
PUT https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productGuid": "string",
  "productCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productGuid": "string",
    "productCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productGuid` | string | yes | The Unleashed product GUID. |
| `productCode` | string | yes | Product code required by the Unleashed update contract. |
| `productDescription` | string | no | Updated description for the product. |
| `obsolete` | boolean | no | Marks the product obsolete for cleanup. |

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

Through the native Unleashed API, this operation is `POST /Products/:productGuid` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

