# Dropbox: List File Revisions

Retrieves revision history for a file from Dropbox.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-file-revisions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-file-revisions?connectionId=$CONNECTION_ID&path=id%3Aa4ayc_80_OEAAAAAAAAAYa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "id:a4ayc_80_OEAAAAAAAAAYa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-file-revisions?${params}`, {
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
| `path` | string | yes | The file path or ID to list revisions for. Example: `id:a4ayc_80_OEAAAAAAAAAYa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        {
          "clientModified": "2026-05-07T12:00:00.000Z",
          "contentHash": "string",
          "id": "string",
          "isDownloadable": true,
          "name": "Ava Chen",
          "pathDisplay": "string",
          "pathLower": "string",
          "rev": "string",
          "serverModified": "2026-05-07T12:00:00.000Z",
          "size": 1
        }
      ],
      "hasMore": true,
      "isDeleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries[].clientModified` | date |  |
| `entries[].contentHash` | string |  |
| `entries[].id` | string |  |
| `entries[].isDownloadable` | boolean |  |
| `entries[].name` | string |  |
| `entries[].pathDisplay` | string |  |
| `entries[].pathLower` | string |  |
| `entries[].rev` | string |  |
| `entries[].serverModified` | date |  |
| `entries[].size` | number |  |
| `hasMore` | boolean |  |
| `isDeleted` | boolean |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /files/list_revisions` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-file-revisions.md) for the provider-specific parameters and requirements.

