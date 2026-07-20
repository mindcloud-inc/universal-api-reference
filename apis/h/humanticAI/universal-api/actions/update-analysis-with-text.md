# Humantic AI: Update Analysis With Text



```
PUT https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/update-analysis-with-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Humantic AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/update-analysis-with-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/update-analysis-with-text', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The same identifier used when the original analysis was created. |
| `text` | string | yes | Additional text to improve confidence for an existing Humantic AI analysis. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "results": {
        "last_modified": "2026-05-07T12:00:00.000Z",
        "userid": "string",
        "username": "Ava Chen"
      },
      "status": "string",
      "usage_stats": {
        "user_profile": {
          "consumed": 1,
          "limit": 1,
          "remaining": 1,
          "subscription_status": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `results.last_modified` | date |  |
| `results.userid` | string |  |
| `results.username` | string |  |
| `status` | string |  |
| `usage_stats.user_profile.consumed` | number |  |
| `usage_stats.user_profile.limit` | number |  |
| `usage_stats.user_profile.remaining` | number |  |
| `usage_stats.user_profile.subscription_status` | string |  |

## Native endpoint

Through the native Humantic AI API, this operation is `POST /user-profile/create` (base URL `https://api.humantic.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-analysis-with-text.md) for the provider-specific parameters and requirements.

