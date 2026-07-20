# Neon: Create snapshot

Creates a snapshot in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-snapshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "branch_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-snapshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "branch_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | yes | Neon API parameter project_id |
| `branch_id` | string | yes | Neon API parameter branch_id |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lsn` | string | no | Neon API parameter lsn |
| `timestamp` | string | no | Neon API parameter timestamp |
| `name` | string | no | Neon API parameter name |
| `expires_at` | string | no | Neon API parameter expires_at |

## Response

```json
{
  "success": true,
  "data": [
    {
      "operations": [
        {}
      ],
      "snapshot": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `operations` | array<object> |  |
| `snapshot` | object |  |

## Native endpoint

Through the native Neon API, this operation is `POST /projects/:project_id/branches/:branch_id/snapshot` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-snapshot.md) for the provider-specific parameters and requirements.

