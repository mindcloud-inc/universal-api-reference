# Zoho Inventory: Get Item

Retrieves an item from Zoho Inventory.

```
GET https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/get-item?connectionId=$CONNECTION_ID&itemId=string&organizationId=%7B%7Bcredentials.organizationId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "string",
  "organizationId": "{{credentials.organizationId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/get-item?${params}`, {
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
| `itemId` | string | yes | The Zoho Inventory item_id for the item. |
| `organizationId` | string | yes | Zoho Inventory organization ID to run this request against. Default: `{{credentials.organizationId}}`. |

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

Through the native Zoho Inventory API, this operation is `GET /items/:item_id` (base URL `{{credentials.accessTokenRequest.api_domain}}/inventory/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

