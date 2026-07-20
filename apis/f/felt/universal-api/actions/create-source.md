# Felt: Create Source

Creates a new data source in Felt.

```
POST https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "connection": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "connection": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Source name. |
| `connection` | object | yes | Source connection object matching the Felt source type contract. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `permissions` | object | no | Optional permissions object such as source_owner, workspace_editors, or project_editors. |

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

Through the native Felt API, this operation is `POST /sources` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-source.md) for the provider-specific parameters and requirements.

