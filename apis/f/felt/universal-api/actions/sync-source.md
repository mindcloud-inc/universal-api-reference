# Felt: Sync Source

Syncs a data source in Felt.

```
PUT https://connect.mindcloud.co/v1/universal/felt/latest/actions/sync-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/felt/latest/actions/sync-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/sync-source', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | yes | The Felt source ID. |

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
| `automatic_sync` | string |  |
| `connection_type` | string |  |
| `id` | string |  |
| `links` | object |  |
| `name` | string |  |
| `owner_id` | string |  |
| `permissions` | object |  |
| `sync_status` | string |  |
| `type` | string |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native Felt API, this operation is `POST /sources/:sourceId/sync` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sync-source.md) for the provider-specific parameters and requirements.

