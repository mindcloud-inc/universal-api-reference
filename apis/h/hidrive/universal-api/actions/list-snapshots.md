# HiDrive: List Snapshots

Retrieves snapshots from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-snapshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-snapshots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-snapshots?${params}`, {
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
| `path` | string | no | Path to list snapshots for. |
| `pid` | string | no | Object public ID to list snapshots for. |
| `scope` | string | no | Snapshot scope, defaults to user. Default: `user`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automatic": true,
      "date": 1,
      "name": "Ava Chen",
      "zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automatic` | boolean | Whether the snapshot was created automatically. |
| `date` | number | Snapshot timestamp. |
| `name` | string | Snapshot name. |
| `zone` | string | Snapshot zone. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /snapshot` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-snapshots.md) for the provider-specific parameters and requirements.

