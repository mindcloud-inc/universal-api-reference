# Release0: List Agents

Retrieves agents in a Release0 workspace.

```
GET https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Release0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-agents?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-agents?${params}`, {
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
| `workspaceId` | string | yes | The workspace ID to list agents from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "domainId": "string",
      "icon": "string",
      "id": "string",
      "isPublished": true,
      "name": "Ava Chen",
      "publicId": "string",
      "publishedAt": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `domainId` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `isPublished` | boolean |  |
| `name` | string |  |
| `publicId` | string |  |
| `publishedAt` | string |  |
| `tags` | array<string> |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Release0 API, this operation is `GET /v1/agents` (base URL `https://release0.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

