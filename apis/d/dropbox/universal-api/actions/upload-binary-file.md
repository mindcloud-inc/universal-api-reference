# Dropbox: Upload Binary File



```
POST https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/upload-binary-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/upload-binary-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "path": "/Homework/math/Matrices.pdf",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/upload-binary-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "path": "/Homework/math/Matrices.pdf",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | yes | Example: `/Homework/math/Matrices.pdf`. |
| `file` | file | yes | Base64-encoded file content or an accessible HTTP(S) download URL. Sends the original bytes as the request body. Maximum 100 MiB. |
| `mode` | list<string> | no | Add creates a file; overwrite replaces existing content. Revision-conditional update is not supported by this action. One of: `add`, `overwrite`. Default: `add`. Example: `add`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `autorename` | boolean | no | Default: `false`. |
| `mute` | boolean | no | Default: `false`. |
| `strictConflict` | boolean | no | Default: `false`. |

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

Through the native Dropbox API, this operation is `POST https://content.dropboxapi.com/2/files/upload` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-binary-file.md) for the provider-specific parameters and requirements.

