# Cursor: List Agent Artifacts



```
GET https://connect.mindcloud.co/v1/universal/cursor/latest/actions/list-agent-artifacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursor/latest/actions/list-agent-artifacts?connectionId=$CONNECTION_ID&id=bc_abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "bc_abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursor/latest/actions/list-agent-artifacts?${params}`, {
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
| `id` | string | yes | Unique identifier for the cloud agent whose artifacts should be listed. Example: `bc_abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "absolutePath": "string",
      "sizeBytes": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absolutePath` | string | Absolute artifact path in the cloud agent environment. |
| `sizeBytes` | number | Artifact file size in bytes. |
| `updatedAt` | date | Last modified timestamp for the artifact. |

## Native endpoint

Through the native Cursor API, this operation is `GET /v0/agents/{{id}}/artifacts` (base URL `https://api.cursor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agent-artifacts.md) for the provider-specific parameters and requirements.

