# inFlow Inventory: Insert or Update Product

Inserts or updates a product in inFlow Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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

Through the native inFlow Inventory API, this operation is `PUT /products` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-or-update-product.md) for the provider-specific parameters and requirements.

