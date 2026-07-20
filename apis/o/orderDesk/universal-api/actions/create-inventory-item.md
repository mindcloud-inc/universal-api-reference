# Order Desk: Create Inventory Item

Creates a new inventory item in Order Desk.

```
POST https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/create-inventory-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/create-inventory-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/create-inventory-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Display name of the inventory item. |
| `code` | string | yes | Unique SKU code for the inventory item. |
| `price` | number | no | Item price. |
| `stock` | number | no | Available stock quantity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionTime": "string",
      "inventoryItem": {},
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
| `inventoryItem` | object |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Order Desk API, this operation is `POST /inventory-items` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inventory-item.md) for the provider-specific parameters and requirements.

