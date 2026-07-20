# Lokalise: Restore Snapshot

Restores a snapshot in a Lokalise project.

```
POST https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/restore-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lokalise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/restore-snapshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/restore-snapshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | no | Lokalise project identifier. |
| `snapshot_id` | string | no | Lokalise snapshot identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "project_id": "string",
      "project_uuid": "string",
      "snapshot": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `project_id` | string |  |
| `project_uuid` | string |  |
| `snapshot` | object |  |

## Native endpoint

Through the native Lokalise API, this operation is `POST /projects/:project_id/snapshots/:snapshot_id` (base URL `https://api.lokalise.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-snapshot.md) for the provider-specific parameters and requirements.

