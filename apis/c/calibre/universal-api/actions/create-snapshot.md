# Calibre: Create Snapshot

Creates a new snapshot for a site in Calibre.

```
POST https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-snapshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.site": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-snapshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.site": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.site` | string | yes | Site slug, found in site settings. |
| `variables.ref` | string | no | Reference label for this snapshot, such as a commit SHA or branch name. |
| `variables.client` | string | no | Client name that created the snapshot. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createSnapshot": {
        "client": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "htmlUrl": "https://example.com",
        "id": "string",
        "iid": 1,
        "ref": "string",
        "status": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
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
| `createSnapshot.client` | string |  |
| `createSnapshot.createdAt` | date |  |
| `createSnapshot.htmlUrl` | string |  |
| `createSnapshot.id` | string |  |
| `createSnapshot.iid` | number |  |
| `createSnapshot.ref` | string |  |
| `createSnapshot.status` | string |  |
| `createSnapshot.updatedAt` | date |  |
| `createSnapshot.uuid` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-snapshot.md) for the provider-specific parameters and requirements.

