# Orq.ai: Create Agent

Creates a new agent in Orq.ai.

```
POST https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "description": "string",
      "engine": "string",
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
| `engine` | string |  |
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

Through the native Orq.ai API, this operation is `POST /v2/agents` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent.md) for the provider-specific parameters and requirements.

