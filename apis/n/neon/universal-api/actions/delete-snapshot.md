# Neon: Delete snapshot

Deletes a snapshot from Neon.

```
DELETE https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-snapshot?connectionId=$CONNECTION_ID&project_id=string&snapshot_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "snapshot_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-snapshot?${params}`, {
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
| `project_id` | string | yes | Neon API parameter project_id |
| `snapshot_id` | string | yes | Neon API parameter snapshot_id |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `operations` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `DELETE /projects/:project_id/snapshots/:snapshot_id` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-snapshot.md) for the provider-specific parameters and requirements.

