# Calibre: List Snapshots

Retrieves snapshots for a site from Calibre.

```
GET https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-snapshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-snapshots?connectionId=$CONNECTION_ID&variables.site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-snapshots?${params}`, {
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
| `variables.first` | number | no | Maximum number of snapshots to return. Default: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organisation": {
        "site": {
          "snapshotsList": {
            "nodes": [
              {
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
            ],
            "pageInfo": {
              "endCursor": "string",
              "hasNextPage": true,
              "hasPreviousPage": true,
              "startCursor": "string"
            }
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organisation.site.snapshotsList.nodes[].client` | string |  |
| `organisation.site.snapshotsList.nodes[].createdAt` | date |  |
| `organisation.site.snapshotsList.nodes[].htmlUrl` | string |  |
| `organisation.site.snapshotsList.nodes[].id` | string |  |
| `organisation.site.snapshotsList.nodes[].iid` | number |  |
| `organisation.site.snapshotsList.nodes[].ref` | string |  |
| `organisation.site.snapshotsList.nodes[].status` | string |  |
| `organisation.site.snapshotsList.nodes[].updatedAt` | date |  |
| `organisation.site.snapshotsList.nodes[].uuid` | string |  |
| `organisation.site.snapshotsList.pageInfo.endCursor` | string |  |
| `organisation.site.snapshotsList.pageInfo.hasNextPage` | boolean |  |
| `organisation.site.snapshotsList.pageInfo.hasPreviousPage` | boolean |  |
| `organisation.site.snapshotsList.pageInfo.startCursor` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-snapshots.md) for the provider-specific parameters and requirements.

