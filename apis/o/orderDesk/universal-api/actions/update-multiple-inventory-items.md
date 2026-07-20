# Order Desk: Update Multiple Inventory Items

Updates multiple inventory items in Order Desk.

```
PUT https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/update-multiple-inventory-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/update-multiple-inventory-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inventoryItems[].id": "string",
  "inventoryItems[].name": "Ava Chen",
  "inventoryItems[].code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/update-multiple-inventory-items', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inventoryItems[].id": "string",
    "inventoryItems[].name": "Ava Chen",
    "inventoryItems[].code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inventoryItems[].id` | string | yes | Order Desk internal inventory item ID. |
| `inventoryItems[].name` | string | yes | Display name of the inventory item. |
| `inventoryItems[].code` | string | yes | Unique SKU code for the inventory item. |
| `inventoryItems[].price` | number | no | Item price. |
| `inventoryItems[].stock` | number | no | Available stock quantity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionTime": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `executionTime` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Order Desk API, this operation is `PUT /batch-inventory-items` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-multiple-inventory-items.md) for the provider-specific parameters and requirements.

