# Uwear.ai: Create New Clothing Item

Creates a new clothing item in Uwear.ai.

```
POST https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/create-new-clothing-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uwear.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/create-new-clothing-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clothing_item_name": "Ava Chen",
  "description": "string",
  "description_back": "string",
  "external_clothing_item_url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/create-new-clothing-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clothing_item_name": "Ava Chen",
    "description": "string",
    "description_back": "string",
    "external_clothing_item_url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clothing_item_name` | string | yes | Human-readable clothing item name. |
| `description` | string | yes | Text description of the clothing item front view. |
| `description_back` | string | yes | Text description of the clothing item back view. |
| `external_clothing_item_back_url` | string | no | Optional publicly fetchable direct image URL for the clothing item back view. |
| `external_clothing_item_url` | string | yes | Publicly fetchable direct image URL for the clothing item front view. |
| `use_image_enhancement` | boolean | no | Enable Uwear image enhancement before processing. Default: `false`. |

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

Through the native Uwear.ai API, this operation is `POST /api/v1/clothing-item` (base URL `https://api.uwear.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-new-clothing-item.md) for the provider-specific parameters and requirements.

