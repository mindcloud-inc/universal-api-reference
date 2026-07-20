# Letta: Summarize Agent Messages

Summarizes an agent's conversation history in Letta.

```
POST https://connect.mindcloud.co/v1/universal/letta/latest/actions/summarize-agent-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Letta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/letta/latest/actions/summarize-agent-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/letta/latest/actions/summarize-agent-messages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The Letta agent ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `compactionSettings` | object | no | Optional Letta compaction settings. Use mode all when summarizing short test conversations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "num_messages_after": 1,
      "num_messages_before": 1,
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `num_messages_after` | number |  |
| `num_messages_before` | number |  |
| `summary` | string |  |

## Native endpoint

Through the native Letta API, this operation is `POST /v1/agents/:agent_id/summarize` (base URL `https://api.letta.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/summarize-agent-messages.md) for the provider-specific parameters and requirements.

