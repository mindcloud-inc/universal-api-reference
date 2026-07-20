# Calibre: Download Snapshot Artifacts

Retrieves artifact download URLs for a snapshot from Calibre.

```
GET https://connect.mindcloud.co/v1/universal/calibre/latest/actions/download-snapshot-artifacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/download-snapshot-artifacts?connectionId=$CONNECTION_ID&variables.site=string&variables.snapshotIid=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.site": "string",
  "variables.snapshotIid": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/download-snapshot-artifacts?${params}`, {
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
| `variables.snapshotIid` | number | yes | Snapshot IID used by the documented snapshot APIs. |
| `variables.artifactName` | string | no | Snapshot test artifact enum value. Default: `TEST_ARTIFACT_LIGHTHOUSE`. |
| `variables.mediaName` | string | no | Snapshot media enum value. Default: `TEST_MEDIA_IMAGE`. |

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
                "htmlUrl": "https://example.com",
                "id": "string",
                "iid": 1,
                "status": "string",
                "tests": [
                  {
                    "artifactURL": "https://example.com",
                    "mediaURL": "https://example.com",
                    "status": "string",
                    "uuid": "string"
                  }
                ],
                "uuid": "string"
              }
            ]
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
| `organisation.site.snapshotsList.nodes[].htmlUrl` | string |  |
| `organisation.site.snapshotsList.nodes[].id` | string |  |
| `organisation.site.snapshotsList.nodes[].iid` | number |  |
| `organisation.site.snapshotsList.nodes[].status` | string |  |
| `organisation.site.snapshotsList.nodes[].tests[].artifactURL` | string |  |
| `organisation.site.snapshotsList.nodes[].tests[].mediaURL` | string |  |
| `organisation.site.snapshotsList.nodes[].tests[].status` | string |  |
| `organisation.site.snapshotsList.nodes[].tests[].uuid` | string |  |
| `organisation.site.snapshotsList.nodes[].uuid` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-snapshot-artifacts.md) for the provider-specific parameters and requirements.

