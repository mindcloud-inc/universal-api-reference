# Botbaba: Update Product Inventory Total



```
PUT https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/update-product-inventory-total
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botbaba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/update-product-inventory-total" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": 1,
  "inventoryDetails[]": [
    {}
  ],
  "inventoryDetails[].sku": "string",
  "inventoryDetails[].InventoryQty": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/update-product-inventory-total', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": 1,
    "inventoryDetails[]": [{}],
    "inventoryDetails[].sku": "string",
    "inventoryDetails[].InventoryQty": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | number | yes | Bot identifier. |
| `inventoryDetails[]` | array<object> | yes | Inventory detail rows. |
| `inventoryDetails[].sku` | string | yes | Product SKU. |
| `inventoryDetails[].InventoryQty` | number | yes | Inventory quantity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | boolean |  |

## Native endpoint

Through the native Botbaba API, this operation is `POST /api/EditProductInventoryTotal` (base URL `https://app.botbaba.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-inventory-total.md) for the provider-specific parameters and requirements.

