# Dropbox: Restore File Revision

Restores a file revision in Dropbox.

```
PUT https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/restore-file-revision
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/restore-file-revision" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "path": "/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/restore-target.txt",
  "rev": "0164c60e146fb1a00000002c9f7ce53"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/restore-file-revision', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "path": "/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/restore-target.txt",
    "rev": "0164c60e146fb1a00000002c9f7ce53"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | yes | Dropbox path for the file revision to restore. Example: `/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/restore-target.txt`. |
| `rev` | string | yes | Revision identifier to restore. Example: `0164c60e146fb1a00000002c9f7ce53`. |

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

Through the native Dropbox API, this operation is `POST /files/restore` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-file-revision.md) for the provider-specific parameters and requirements.

