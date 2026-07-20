# Release0: List Linked Agents

Retrieves agents linked to a Release0 agent.

```
GET https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-linked-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Release0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-linked-agents?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-linked-agents?${params}`, {
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
      "agents": [
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
| `agents` | array<object> | Linked agents returned by Release0. |

## Native endpoint

Through the native Release0 API, this operation is `GET /v1/agents/:agentId/linkedAgents` (base URL `https://release0.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-linked-agents.md) for the provider-specific parameters and requirements.

