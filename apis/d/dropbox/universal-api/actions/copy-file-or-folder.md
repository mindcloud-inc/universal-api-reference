# Dropbox: Copy File or Folder

Creates a copy of a file or folder in Dropbox.

```
POST https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/copy-file-or-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/copy-file-or-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fromPath": "/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/restore-target.txt",
  "toPath": "/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/copy-target.txt"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/copy-file-or-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fromPath": "/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/restore-target.txt",
    "toPath": "/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/copy-target.txt"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromPath` | string | yes | Source Dropbox path to copy. Example: `/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/restore-target.txt`. |
| `toPath` | string | yes | Destination Dropbox path for the copy. Example: `/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/copy-target.txt`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `autorename` | boolean | no | Automatically rename the copied item on conflict. Default: `false`. Example: `false`. |

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

Through the native Dropbox API, this operation is `POST /files/copy_v2` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-file-or-folder.md) for the provider-specific parameters and requirements.

