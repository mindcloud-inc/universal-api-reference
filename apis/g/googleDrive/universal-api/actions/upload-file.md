# Google Drive: Upload File

Uploads a new file to Google Drive.

```
POST https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileType": "application/pdf",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileType": "application/pdf",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileType` | list | yes | MIME type of the uploaded file. Supports PDF, Excel, Word, GIF, PNG, JPEG, CSV, plain text, and Markdown. One of: `application/pdf`, `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet`, `application/vnd.openxmlformats-officedocument.wordprocessingml.document`, `image/gif`, `image/jpeg`, `image/png`, `text/csv`, `text/markdown`, `text/plain`. |
| `file` | file | yes | Base64-encoded file content or a direct download URL that works without interactive sign-in. Supports PDF, Excel, Word, images, CSV, plain text, and Markdown. This action uploads content only. To set name and folder, call Move File after upload using the returned file ID. Prefer a URL for larger files. The Universal API execution timeout still applies. |
| `fileName` | string | no | Not accepted by Upload File. After uploading content, use Move File with the returned fileId and the desired name. |
| `parentFolderId` | list<string> | no | Not accepted by Upload File. After uploading content, use Move File with the returned fileId and the destination folder ID as addParents. |

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

Through the native Google Drive API, this operation is `POST /upload/drive/v3/files` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

