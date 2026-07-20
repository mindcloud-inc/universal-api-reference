# Uwear.ai: Save Avatar

Creates an avatar from a generation result in Uwear.ai.

```
POST https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/save-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uwear.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/save-avatar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "avatar_name": "Ava Chen",
  "generation_result_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/save-avatar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "avatar_name": "Ava Chen",
    "generation_result_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `avatar_description` | string | no | Optional avatar description. |
| `avatar_name` | string | yes | Avatar name. |
| `generation_result_id` | number | yes | Generation result ID to save as an avatar. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "age": 1,
      "avatar_description": "string",
      "avatar_id": 1,
      "avatar_name": "Ava Chen",
      "avatar_url": "https://example.com",
      "body": "string",
      "created_at": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | number |  |
| `avatar_description` | string |  |
| `avatar_id` | number |  |
| `avatar_name` | string |  |
| `avatar_url` | string |  |
| `body` | string |  |
| `created_at` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Uwear.ai API, this operation is `POST /api/v1/avatar` (base URL `https://api.uwear.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-avatar.md) for the provider-specific parameters and requirements.

