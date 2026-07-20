# Letta: Update Agent Memory Block

Updates a core memory block in Letta by label.

```
PUT https://connect.mindcloud.co/v1/universal/letta/latest/actions/update-agent-memory-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Letta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/letta/latest/actions/update-agent-memory-block" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "blockLabel": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/letta/latest/actions/update-agent-memory-block', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "blockLabel": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The Letta agent ID. |
| `blockLabel` | string | yes | The label of the memory block attached to the agent. |
| `value` | string | yes | The updated memory block value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "label": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `label` | string |  |
| `updated_at` | date |  |
| `value` | string |  |

## Native endpoint

Through the native Letta API, this operation is `PATCH /v1/agents/:agent_id/core-memory/blocks/:block_label` (base URL `https://api.letta.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent-memory-block.md) for the provider-specific parameters and requirements.

