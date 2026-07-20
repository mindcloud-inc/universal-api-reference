# Orq.ai: Update Agent

Updates an existing agent in Orq.ai.

```
PUT https://connect.mindcloud.co/v1/universal/orqai/latest/actions/update-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/update-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentKey": "agent_test_key"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orqai/latest/actions/update-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentKey": "agent_test_key"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentKey` | string | yes | Agent Key from the Orq.ai path parameter. Example: `agent_test_key`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "description": "string",
      "instructions": "string",
      "key": "string",
      "model": {
        "id": "string"
      },
      "path": "string",
      "role": "string",
      "status": "string",
      "type": "string",
      "updated": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `description` | string |  |
| `instructions` | string |  |
| `key` | string |  |
| `model.id` | string |  |
| `path` | string |  |
| `role` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updated` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Orq.ai API, this operation is `PATCH /v2/agents/[:agent_key]` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent.md) for the provider-specific parameters and requirements.

