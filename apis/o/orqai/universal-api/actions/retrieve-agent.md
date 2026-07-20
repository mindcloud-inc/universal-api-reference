# Orq.ai: Retrieve Agent

Retrieves an agent from Orq.ai.

```
GET https://connect.mindcloud.co/v1/universal/orqai/latest/actions/retrieve-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/retrieve-agent?connectionId=$CONNECTION_ID&agentKey=agent_test_key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentKey": "agent_test_key"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/retrieve-agent?${params}`, {
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

Through the native Orq.ai API, this operation is `GET /v2/agents/[:agent_key]` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-agent.md) for the provider-specific parameters and requirements.

