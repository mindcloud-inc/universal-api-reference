# Uwear.ai: Get Clothing Item Details

Retrieves clothing item details from Uwear.ai.

```
GET https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-clothing-item-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uwear.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-clothing-item-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-clothing-item-details?${params}`, {
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
| `clothing_item_id` | string | no | The clothing item ID. |

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

Through the native Uwear.ai API, this operation is `GET /api/v1/clothing-item/:clothing_item_id` (base URL `https://api.uwear.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-clothing-item-details.md) for the provider-specific parameters and requirements.

