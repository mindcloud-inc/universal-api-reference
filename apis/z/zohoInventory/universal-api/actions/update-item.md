# Zoho Inventory: Update Item

Updates an existing item in Zoho Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/update-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/update-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "string",
  "organizationId": "{{credentials.organizationId}}",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/update-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "string",
    "organizationId": "{{credentials.organizationId}}",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | string | yes | The Zoho Inventory item_id for the item. |
| `organizationId` | string | yes | Zoho Inventory organization ID to run this request against. Default: `{{credentials.organizationId}}`. |
| `name` | string | yes | Display name of the item. |
| `rate` | number | no | Sales rate for the item. |
| `description` | string | no | Description for the item. |
| `sku` | string | no | Stock keeping unit for the item. |
| `itemType` | string | no | Type of item to update. Default: `sales`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_time": "string",
      "description": "string",
      "item_id": "string",
      "item_type": "string",
      "last_modified_time": "string",
      "name": "Ava Chen",
      "product_type": "string",
      "rate": 1,
      "sku": "string",
      "status": "string",
      "track_inventory": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_time` | string |  |
| `description` | string |  |
| `item_id` | string |  |
| `item_type` | string |  |
| `last_modified_time` | string |  |
| `name` | string |  |
| `product_type` | string |  |
| `rate` | number |  |
| `sku` | string |  |
| `status` | string |  |
| `track_inventory` | boolean |  |

## Native endpoint

Through the native Zoho Inventory API, this operation is `PUT /items/:item_id` (base URL `{{credentials.accessTokenRequest.api_domain}}/inventory/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item.md) for the provider-specific parameters and requirements.

