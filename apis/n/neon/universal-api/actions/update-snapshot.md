# Neon: Update snapshot

Updates a snapshot in Neon.

```
PUT https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-snapshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "snapshot_id": "string",
  "snapshot": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-snapshot', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "snapshot_id": "string",
    "snapshot": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | yes | Neon API parameter project_id |
| `snapshot_id` | string | yes | Neon API parameter snapshot_id |
| `snapshot` | object | yes | Neon API parameter snapshot |

## Response

```json
{
  "success": true,
  "data": [
    {
      "snapshot": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `snapshot` | object |  |

## Native endpoint

Through the native Neon API, this operation is `PATCH /projects/:project_id/snapshots/:snapshot_id` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-snapshot.md) for the provider-specific parameters and requirements.

