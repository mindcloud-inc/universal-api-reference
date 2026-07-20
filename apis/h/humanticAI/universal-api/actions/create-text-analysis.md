# Humantic AI: Create Text Analysis



```
POST https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/create-text-analysis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Humantic AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/create-text-analysis" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/create-text-analysis', {
  method: 'POST',
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
| `id` | string | yes | Unique identifier for the text analysis. Do not use values starting with `test`. |
| `text` | string | yes | Free-form text to analyze. Humantic recommends at least 300 words and processes only the first 10,000 words. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stateless` | boolean | no | When true, Humantic does not save text input data. Applies only to text or document input. |
| `analysistype` | string | no | Use `talent` for English text or document input intended for hiring or talent assessment. Example: `talent`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "results": {
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
| `results.userid` | string |  |
| `results.username` | string |  |
| `status` | string |  |
| `usage_stats.user_profile.consumed` | number |  |
| `usage_stats.user_profile.limit` | number |  |
| `usage_stats.user_profile.remaining` | number |  |
| `usage_stats.user_profile.subscription_status` | string |  |

## Native endpoint

Through the native Humantic AI API, this operation is `POST /user-profile/create` (base URL `https://api.humantic.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-analysis.md) for the provider-specific parameters and requirements.

