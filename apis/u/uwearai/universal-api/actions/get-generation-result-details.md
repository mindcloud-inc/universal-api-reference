# Uwear.ai: Get Generation Result Details

Retrieves generation result details from Uwear.ai.

```
GET https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-generation-result-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uwear.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-generation-result-details?connectionId=$CONNECTION_ID&generation_result_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "generation_result_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-generation-result-details?${params}`, {
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
| `generation_result_id` | number | yes | Generation result ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "generation_id": 1,
      "generation_result_id": 1,
      "image_url": "https://example.com",
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
| `created_at` | string |  |
| `generation_id` | number |  |
| `generation_result_id` | number |  |
| `image_url` | string |  |
| `status` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Uwear.ai API, this operation is `GET /api/v1/generation-result/:generation_result_id` (base URL `https://api.uwear.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-generation-result-details.md) for the provider-specific parameters and requirements.

