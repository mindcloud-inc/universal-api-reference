# Google Drive: Move File

Move a File to a Folder.

```
PUT https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/move-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/move-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addParents": "string",
  "fileId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/move-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addParents": "string",
    "fileId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addParents` | string | yes | Comma-separated parent folder IDs to add. For single-folder move, pass the destination folder ID. |
| `removeParents` | string | no | Comma-separated parent folder IDs to remove. Optional when only adding a parent. |
| `fileId` | string | yes | Specify the 'fileId' of a File to move. Select a File in the list or use "Search Files & Folders" to get another File in your Drive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "kind": "string",
      "mimeType": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `kind` | string |  |
| `mimeType` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Google Drive API, this operation is `PATCH /drive/v3/files/:fileId` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-file.md) for the provider-specific parameters and requirements.

