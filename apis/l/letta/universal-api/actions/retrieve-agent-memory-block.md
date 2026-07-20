# Letta: Retrieve Agent Memory Block

Retrieves a core memory block from Letta by label.

```
GET https://connect.mindcloud.co/v1/universal/letta/latest/actions/retrieve-agent-memory-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Letta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/letta/latest/actions/retrieve-agent-memory-block?connectionId=$CONNECTION_ID&agentId=string&blockLabel=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string",
  "blockLabel": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/letta/latest/actions/retrieve-agent-memory-block?${params}`, {
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
| `agentId` | string | yes | The Letta agent ID. |
| `blockLabel` | string | yes | The label of the memory block attached to the agent. |

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

Through the native Letta API, this operation is `GET /v1/agents/:agent_id/core-memory/blocks/:block_label` (base URL `https://api.letta.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-agent-memory-block.md) for the provider-specific parameters and requirements.

