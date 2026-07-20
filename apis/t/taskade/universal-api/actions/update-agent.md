# Taskade: Update Agent

Updates an existing agent in Taskade.

```
PUT https://connect.mindcloud.co/v1/universal/taskade/latest/actions/update-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Taskade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/taskade/latest/actions/update-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "name": "Ava Chen",
  "data.commands[].name": "Ava Chen",
  "data.commands[].prompt": "string",
  "data.description": "string",
  "data.avatar.data.value": "🤖"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taskade/latest/actions/update-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "name": "Ava Chen",
    "data.commands[].name": "Ava Chen",
    "data.commands[].prompt": "string",
    "data.description": "string",
    "data.avatar.data.value": "🤖"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | Agent ID. |
| `name` | string | yes | Agent name. |
| `data.commands[].name` | string | yes | Single command display name. |
| `data.commands[].prompt` | string | yes | Single command prompt text. |
| `data.description` | string | yes | Agent description. |
| `data.avatar.data.value` | string | yes | Avatar emoji value. Default: `🤖`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "name": "Ava Chen",
      "spaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Agent configuration payload. |
| `id` | string | Agent ID. |
| `name` | string | Agent name. |
| `spaceId` | string | Folder or space ID. |

## Native endpoint

Through the native Taskade API, this operation is `PATCH /agents/:agentId` (base URL `https://www.taskade.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent.md) for the provider-specific parameters and requirements.

