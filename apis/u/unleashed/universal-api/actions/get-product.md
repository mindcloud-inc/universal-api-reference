# Unleashed: Get Product

Retrieves a product from your Unleashed inventory catalog.

```
GET https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/get-product?connectionId=$CONNECTION_ID&productGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/get-product?${params}`, {
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
| `productGuid` | string | yes | The Unleashed product GUID. |

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

Through the native Unleashed API, this operation is `GET /Products/:productGuid` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

