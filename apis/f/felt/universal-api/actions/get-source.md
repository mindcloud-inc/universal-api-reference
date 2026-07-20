# Felt: Get Source

Retrieves a data source from Felt.

```
GET https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-source?connectionId=$CONNECTION_ID&sourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-source?${params}`, {
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
| `sourceId` | string | yes | Source ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automatic_sync": "string",
      "connection": {},
      "connection_type": "string",
      "datasets": [
        {}
      ],
      "id": "string",
      "last_synced_at": 1,
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
| `connection` | object | Source connection configuration. |
| `connection_type` | string | Configured source connection type. |
| `datasets` | array<object> | Datasets discovered on the source. |
| `id` | string | Felt source ID. |
| `last_synced_at` | number | Most recent sync timestamp. |
| `name` | string | Source name. |
| `owner_id` | string | Owning user ID. |
| `permissions` | object | Source permissions. |
| `sync_status` | string | Inspection status for the source. |
| `type` | string | Returned resource type. |
| `workspace_id` | string | Workspace that owns the source. |

## Native endpoint

Through the native Felt API, this operation is `GET /sources/:sourceId` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-source.md) for the provider-specific parameters and requirements.

