# Dropbox: Get File or Folder Metadata

Retrieves file or folder metadata from Dropbox.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-file-or-folder-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-file-or-folder-metadata?connectionId=$CONNECTION_ID&path=id%3Aa4ayc_80_OEAAAAAAAAAYa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "id:a4ayc_80_OEAAAAAAAAAYa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-file-or-folder-metadata?${params}`, {
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
| `path` | string | yes | The file or folder path or ID to fetch metadata for. Example: `id:a4ayc_80_OEAAAAAAAAAYa`. |

## Response

```json
{
  "success": true,
  "data": [
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
      "size": 1,
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientModified` | date |  |
| `contentHash` | string |  |
| `id` | string |  |
| `isDownloadable` | boolean |  |
| `name` | string |  |
| `pathDisplay` | string |  |
| `pathLower` | string |  |
| `rev` | string |  |
| `serverModified` | date |  |
| `size` | number |  |
| `tag` | string |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /files/get_metadata` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-or-folder-metadata.md) for the provider-specific parameters and requirements.

