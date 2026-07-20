# E2B: List Snapshots

Retrieves a list of snapshots from E2B.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-snapshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-snapshots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-snapshots?${params}`, {
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
| `sandboxId` | string | no | Filter snapshots by source sandbox ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "names": [
        "Ava Chen"
      ],
      "snapshotID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `names` | array<string> | Full names of the snapshot template. |
| `snapshotID` | string | Identifier of the snapshot template including tag. |

## Native endpoint

Through the native E2B API, this operation is `GET /snapshots` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-snapshots.md) for the provider-specific parameters and requirements.

