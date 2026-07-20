# Dropbox: Delete File or Folder

Deletes an existing file or folder from Dropbox.

```
DELETE https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/delete-file-or-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/delete-file-or-folder?connectionId=$CONNECTION_ID&path=%2FMindCloud%20Dropbox%20Test%2Fdropbox-stage3-20260306-171004%2Fmoved-target.txt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/moved-target.txt"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/delete-file-or-folder?${params}`, {
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
| `path` | string | yes | Dropbox path of the file or folder to delete. Example: `/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/moved-target.txt`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parentRev` | string | no | Optional parent revision for safer deletes. Example: `0164c60eb6a1da000000002c9f7ce53`. |

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

Through the native Dropbox API, this operation is `POST /files/delete_v2` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file-or-folder.md) for the provider-specific parameters and requirements.

