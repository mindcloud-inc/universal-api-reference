# Release0: List Agent Result Logs

Retrieves execution logs for a Release0 agent result.

```
GET https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-agent-result-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Release0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-agent-result-logs?connectionId=$CONNECTION_ID&agentId=string&resultId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string",
  "resultId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-agent-result-logs?${params}`, {
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
| `resultId` | string | yes | The result ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "logs": [
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
| `logs` | array<object> | Execution logs for the specified result. |

## Native endpoint

Through the native Release0 API, this operation is `GET /v1/agents/:agentId/results/:resultId/logs` (base URL `https://release0.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agent-result-logs.md) for the provider-specific parameters and requirements.

