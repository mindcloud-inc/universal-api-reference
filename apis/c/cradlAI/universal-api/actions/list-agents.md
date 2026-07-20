# Cradl AI: List Agents

Retrieves all agents from Cradl AI.

```
GET https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/list-agents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/list-agents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Cradl AI API, this operation is `GET /agents` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

