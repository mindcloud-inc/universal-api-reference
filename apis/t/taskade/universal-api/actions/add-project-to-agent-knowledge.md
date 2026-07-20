# Taskade: Add Project To Agent Knowledge

Adds a project to a Taskade agent knowledge base.

```
POST https://connect.mindcloud.co/v1/universal/taskade/latest/actions/add-project-to-agent-knowledge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Taskade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/taskade/latest/actions/add-project-to-agent-knowledge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taskade/latest/actions/add-project-to-agent-knowledge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The agent ID. |
| `projectId` | string | yes | The project ID to add to the agent knowledge base. |

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
| `data` | object | Updated agent configuration payload. |
| `id` | string | Agent ID. |
| `name` | string | Agent name. |
| `spaceId` | string | Folder or space ID. |

## Native endpoint

Through the native Taskade API, this operation is `POST /agents/:agentId/knowledge/project` (base URL `https://www.taskade.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-project-to-agent-knowledge.md) for the provider-specific parameters and requirements.

