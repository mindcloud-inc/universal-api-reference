# Cursor: Delete Agent



```
DELETE https://connect.mindcloud.co/v1/universal/cursor/latest/actions/delete-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cursor/latest/actions/delete-agent?connectionId=$CONNECTION_ID&id=bc_abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "bc_abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursor/latest/actions/delete-agent?${params}`, {
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
| `id` | string | yes | Unique identifier for the cloud agent to delete. Example: `bc_abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Unique cloud agent identifier. |

## Native endpoint

Through the native Cursor API, this operation is `DELETE /v0/agents/{{id}}` (base URL `https://api.cursor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-agent.md) for the provider-specific parameters and requirements.

