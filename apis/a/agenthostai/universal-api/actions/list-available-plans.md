# Agenthost.ai: List Available Plans

Retrieves available subscription plans from Agenthost.ai.

```
GET https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/list-available-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agenthost.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/list-available-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/list-available-plans?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "plans": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `plans` | array<object> | Available plans returned by Agenthost. |

## Native endpoint

Through the native Agenthost.ai API, this operation is `GET /api/openai/available_plans` (base URL `https://api.agenthost.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-plans.md) for the provider-specific parameters and requirements.

