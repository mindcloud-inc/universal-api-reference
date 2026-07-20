# Neon: Restore snapshot

Restores snapshot in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/restore-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/restore-snapshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "snapshot_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/restore-snapshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "snapshot_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Neon API parameter name |
| `project_id` | string | yes | Neon API parameter project_id |
| `snapshot_id` | string | yes | Neon API parameter snapshot_id |
| `name` | string | no | Neon API parameter name |
| `target_branch_id` | string | no | Neon API parameter target_branch_id |
| `finalize_restore` | boolean | no | Neon API parameter finalize_restore |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch": {},
      "endpoints": [
        {}
      ],
      "operations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch` | object |  |
| `endpoints` | array<object> |  |
| `operations` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `POST /projects/:project_id/snapshots/:snapshot_id/restore` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-snapshot.md) for the provider-specific parameters and requirements.

