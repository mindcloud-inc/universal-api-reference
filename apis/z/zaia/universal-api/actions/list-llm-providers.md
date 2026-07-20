# Zaia: List LLM Providers

Retrieves LLM providers from your Zaia workspace.

```
GET https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-llm-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zaia `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-llm-providers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-llm-providers?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "type": "string",
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
| `createdAt` | date | Provider creation timestamp. |
| `id` | string | LLM provider UUID. |
| `name` | string | LLM provider display name. |
| `type` | string | Provider type. |
| `updatedAt` | date | Provider update timestamp. |
| `workspaceId` | string | Workspace UUID that owns the provider. |

## Native endpoint

Through the native Zaia API, this operation is `GET /api/v1/llm-providers` (base URL `https://api.endless.zaia.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-llm-providers.md) for the provider-specific parameters and requirements.

