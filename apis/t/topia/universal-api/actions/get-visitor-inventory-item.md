# Topia: Get Visitor Inventory Item

Retrieves a specific visitor inventory item from Topia.

```
GET https://connect.mindcloud.co/v1/universal/topia/latest/actions/get-visitor-inventory-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Topia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topia/latest/actions/get-visitor-inventory-item?connectionId=$CONNECTION_ID&urlSlug=https%3A%2F%2Fexample.com&visitorId=string&itemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlSlug": "https://example.com",
  "visitorId": "string",
  "itemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topia/latest/actions/get-visitor-inventory-item?${params}`, {
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
| `urlSlug` | string | yes | Topia world URL slug. |
| `visitorId` | string | yes | Identifier for the visitor. |
| `itemId` | string | yes | Identifier for the inventory item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "image_url": "https://example.com",
      "interactive_key_id": "string",
      "item_id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "profile_id": "string",
      "quantity": 1,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `image_url` | string |  |
| `interactive_key_id` | string |  |
| `item_id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `profile_id` | string |  |
| `quantity` | number |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Topia API, this operation is `GET /v1/world/:urlSlug/visitors/:visitorId/get-visitor-inventory-items/:itemId` (base URL `https://api.topia.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-visitor-inventory-item.md) for the provider-specific parameters and requirements.

