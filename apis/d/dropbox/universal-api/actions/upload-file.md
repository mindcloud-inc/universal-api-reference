# Dropbox: Upload File

Uploads a new file to Dropbox.

```
POST https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "path": "/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/restore-target.txt",
  "content": "v1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "path": "/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/restore-target.txt",
    "content": "v1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | yes | Dropbox path where the file will be uploaded. Example: `/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/restore-target.txt`. |
| `content` | string | yes | UTF-8 file content to upload. Example: `v1`. |
| `mode` | string | no | Write mode for the upload. Use add to create a new file or overwrite to replace the current content. One of: `0`, `1`. Default: `add`. Example: `add`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `autorename` | boolean | no | Automatically rename the file on conflict. Default: `false`. Example: `false`. |
| `mute` | boolean | no | Suppress notifications for the file update. Default: `false`. Example: `false`. |
| `strictConflict` | boolean | no | Reject writes unless Dropbox can apply the exact requested mode. Default: `false`. Example: `false`. |

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
      "size": 1
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

## Native endpoint

Through the native Dropbox API, this operation is `POST https://content.dropboxapi.com/2/files/upload` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

