# Zaia: List Agents

Retrieves agents from your Zaia workspace.

```
GET https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zaia `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-agents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-agents?${params}`, {
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
| `search` | string | no | Search term to filter agents by name, internal name, role, or prompt. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `squadId` | string | no | Optional squad UUID used to list agents in a specific squad. |
| `versionId` | string | no | Optional version UUID used to list agents for a specific version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "llm": "string",
      "name": "Ava Chen",
      "prompt": "string",
      "role": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Agent creation timestamp. |
| `id` | string | Agent UUID. |
| `llm` | string | LLM model key used by the agent. |
| `name` | string | Agent display name. |
| `prompt` | string | Main agent prompt. |
| `role` | string | Agent role. |
| `updatedAt` | date | Agent update timestamp. |
| `workspaceId` | string | Workspace UUID that owns the agent. |

## Native endpoint

Through the native Zaia API, this operation is `GET /api/v1/agents` (base URL `https://api.endless.zaia.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

