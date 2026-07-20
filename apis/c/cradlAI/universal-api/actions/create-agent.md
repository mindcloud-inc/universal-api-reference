# Cradl AI: Create Agent

Creates a new agent in Cradl AI.

```
POST https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-agent', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Metadata attached to the agent. |
| `name` | string | no | Name of the agent. |
| `description` | string | no | Description of the agent. |
| `resourceIds[]` | array<string> | no | Resources attached to the agent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "createdBy": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "metadata": {},
      "name": "Ava Chen",
      "resourceIds": [
        "string"
      ],
      "updatedBy": "string",
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | Agent identifier. |
| `createdBy` | string | User who created the agent. |
| `createdTime` | date | Timestamp when the agent was created. |
| `description` | string | Agent description. |
| `metadata` | object | Metadata attached to the agent. |
| `name` | string | Agent name. |
| `resourceIds` | array<string> | Resource identifiers attached to the agent. |
| `updatedBy` | string | User who last updated the agent. |
| `updatedTime` | date | Timestamp when the agent was last updated. |

## Native endpoint

Through the native Cradl AI API, this operation is `POST /agents` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent.md) for the provider-specific parameters and requirements.

