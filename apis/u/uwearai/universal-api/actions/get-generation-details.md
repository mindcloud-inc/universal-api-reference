# Uwear.ai: Get Generation Details

Retrieves generation details from Uwear.ai.

```
GET https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-generation-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uwear.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-generation-details?connectionId=$CONNECTION_ID&generation_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "generation_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-generation-details?${params}`, {
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
| `generation_id` | number | yes | Generation request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar_id": 1,
      "clothing_item_ids": [
        1
      ],
      "created_at": "string",
      "feature_name": "Ava Chen",
      "generation_id": 1,
      "generation_results": [
        {}
      ],
      "num_images": 1,
      "outfit_id": 1,
      "payload": "string",
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar_id` | number |  |
| `clothing_item_ids` | array<number> |  |
| `created_at` | string |  |
| `feature_name` | string |  |
| `generation_id` | number |  |
| `generation_results` | array<object> |  |
| `num_images` | number |  |
| `outfit_id` | number |  |
| `payload` | string |  |
| `status` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Uwear.ai API, this operation is `GET /api/v1/generation/:generation_id` (base URL `https://api.uwear.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-generation-details.md) for the provider-specific parameters and requirements.

