# Felt: List Sources

Retrieves data sources from Felt.

```
GET https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-sources?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | no | Optional workspace ID, only needed for plugin contexts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automatic_sync": "string",
      "connection_type": "string",
      "id": "string",
      "links": {},
      "name": "Ava Chen",
      "owner_id": "string",
      "permissions": {},
      "sync_status": "string",
      "type": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automatic_sync` | string | Automatic sync state. |
| `connection_type` | string | Configured source connection type. |
| `id` | string | Felt source ID. |
| `links` | object | Source links. |
| `name` | string | Source name. |
| `owner_id` | string | Owning user ID. |
| `permissions` | object | Source permissions. |
| `sync_status` | string | Inspection status for the source. |
| `type` | string | Returned resource type. |
| `workspace_id` | string | Workspace that owns the source. |

## Native endpoint

Through the native Felt API, this operation is `GET /sources` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sources.md) for the provider-specific parameters and requirements.

