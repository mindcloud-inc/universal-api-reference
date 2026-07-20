# Uwear.ai: Create Edit

Creates an edited generation in Uwear.ai.

```
POST https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/create-edit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uwear.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/create-edit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/create-edit', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `generation_result_id` | number | no | Generation result ID to edit. |
| `image_url` | string | no | Direct image URL to edit. |
| `prompt` | string | yes | Edit prompt. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "feature_name": "Ava Chen",
      "generation_id": 1,
      "generation_results": [
        {}
      ],
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
| `feature_name` | string |  |
| `generation_id` | number |  |
| `generation_results` | array<object> |  |
| `status` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Uwear.ai API, this operation is `POST /api/v1/generation-edit` (base URL `https://api.uwear.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-edit.md) for the provider-specific parameters and requirements.

