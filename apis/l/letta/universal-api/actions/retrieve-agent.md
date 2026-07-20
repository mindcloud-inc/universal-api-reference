# Letta: Retrieve Agent

Retrieves an existing agent from Letta.

```
GET https://connect.mindcloud.co/v1/universal/letta/latest/actions/retrieve-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Letta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/letta/latest/actions/retrieve-agent?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/letta/latest/actions/retrieve-agent?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent_type": "string",
      "id": "string",
      "model": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent_type` | string |  |
| `id` | string |  |
| `model` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Letta API, this operation is `GET /v1/agents/:agent_id` (base URL `https://api.letta.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-agent.md) for the provider-specific parameters and requirements.

