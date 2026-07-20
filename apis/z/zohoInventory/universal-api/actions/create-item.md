# Zoho Inventory: Create Item

Creates a new item in Zoho Inventory.

```
POST https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/create-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "{{credentials.organizationId}}",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `organizationId` | string | yes | Zoho Inventory organization ID to run this request against. Default: `{{credentials.organizationId}}`. |
| `name` | string | yes | Display name of the item. |
| `rate` | number | no | Sales rate for the item. |
| `description` | string | no | Description for the item. |
| `sku` | string | no | Stock keeping unit for the item. |
| `itemType` | string | no | Type of item to create. Default: `sales`. |

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

Through the native Zoho Inventory API, this operation is `POST /items` (base URL `{{credentials.accessTokenRequest.api_domain}}/inventory/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item.md) for the provider-specific parameters and requirements.

