# Uwear.ai: Update Clothing Item

Updates an existing clothing item in Uwear.ai.

```
PUT https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/update-clothing-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uwear.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/update-clothing-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clothing_item_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/update-clothing-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clothing_item_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clothing_item_id` | number | yes | Clothing item ID. |
| `clothing_item_name` | string | no | Updated clothing item name. |
| `description` | string | no | Updated front-view description. |
| `description_back` | string | no | Updated back-view description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clothing_item_back_url": "https://example.com",
      "clothing_item_id": 1,
      "clothing_item_name": "Ava Chen",
      "clothing_item_url": "https://example.com",
      "created_at": "string",
      "description": "string",
      "description_back": "string",
      "external_clothing_item_back_url": "https://example.com",
      "external_clothing_item_url": "https://example.com",
      "gender": "string",
      "product_page_url": "https://example.com",
      "season_color": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clothing_item_back_url` | string |  |
| `clothing_item_id` | number |  |
| `clothing_item_name` | string |  |
| `clothing_item_url` | string |  |
| `created_at` | string |  |
| `description` | string |  |
| `description_back` | string |  |
| `external_clothing_item_back_url` | string |  |
| `external_clothing_item_url` | string |  |
| `gender` | string |  |
| `product_page_url` | string |  |
| `season_color` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Uwear.ai API, this operation is `PUT /api/v1/clothing-item/:clothing_item_id` (base URL `https://api.uwear.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-clothing-item.md) for the provider-specific parameters and requirements.

