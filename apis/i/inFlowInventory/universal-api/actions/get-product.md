# inFlow Inventory: Get Product

Retrieves an existing product from inFlow Inventory.

```
GET https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-product?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-product?${params}`, {
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
| `productId` | string | yes | The inFlow product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoAssemble": true,
      "categoryId": "string",
      "description": "string",
      "height": "string",
      "isActive": true,
      "isManufacturable": true,
      "itemType": "string",
      "lastModifiedById": "string",
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "lastVendorId": "string",
      "length": "string",
      "name": "Ava Chen",
      "productId": "string",
      "purchasingUom": {
        "name": "Ava Chen"
      },
      "salesUom": {
        "name": "Ava Chen"
      },
      "sku": "string",
      "standardUomName": "Ava Chen",
      "timestamp": "string",
      "trackExpiry": true,
      "trackLots": true,
      "trackSerials": true,
      "weight": "string",
      "width": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoAssemble` | boolean |  |
| `categoryId` | string |  |
| `description` | string |  |
| `height` | string |  |
| `isActive` | boolean |  |
| `isManufacturable` | boolean |  |
| `itemType` | string |  |
| `lastModifiedById` | string |  |
| `lastModifiedDateTime` | date |  |
| `lastVendorId` | string |  |
| `length` | string |  |
| `name` | string |  |
| `productId` | string |  |
| `purchasingUom.name` | string |  |
| `salesUom.name` | string |  |
| `sku` | string |  |
| `standardUomName` | string |  |
| `timestamp` | string |  |
| `trackExpiry` | boolean |  |
| `trackLots` | boolean |  |
| `trackSerials` | boolean |  |
| `weight` | string |  |
| `width` | string |  |

## Native endpoint

Through the native inFlow Inventory API, this operation is `GET /products/:productId` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

