# Calibre: Delete Snapshot

Deletes an existing snapshot from Calibre.

```
DELETE https://connect.mindcloud.co/v1/universal/calibre/latest/actions/delete-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/delete-snapshot?connectionId=$CONNECTION_ID&variables.site=string&variables.iid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.site": "string",
  "variables.iid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/delete-snapshot?${params}`, {
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
| `variables.site` | string | yes | Site slug, found in site settings. |
| `variables.iid` | string | yes | Snapshot IID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleteSnapshot": {
        "iid": 1,
        "status": "string",
        "uuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleteSnapshot.iid` | number |  |
| `deleteSnapshot.status` | string |  |
| `deleteSnapshot.uuid` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-snapshot.md) for the provider-specific parameters and requirements.

