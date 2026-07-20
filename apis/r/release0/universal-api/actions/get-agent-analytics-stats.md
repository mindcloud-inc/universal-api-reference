# Release0: Get Agent Analytics Stats

Retrieves analytics stats for a Release0 agent.

```
GET https://connect.mindcloud.co/v1/universal/release0/latest/actions/get-agent-analytics-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Release0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/release0/latest/actions/get-agent-analytics-stats?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/release0/latest/actions/get-agent-analytics-stats?${params}`, {
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
| `agentId` | string | yes | The agent ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "totalCompleted": 1,
      "totalStarts": 1,
      "totalViews": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalCompleted` | number |  |
| `totalStarts` | number |  |
| `totalViews` | number |  |

## Native endpoint

Through the native Release0 API, this operation is `GET /v1/agents/:agentId/analytics/stats` (base URL `https://release0.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-analytics-stats.md) for the provider-specific parameters and requirements.

