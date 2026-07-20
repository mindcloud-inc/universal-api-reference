# Notion: Send File Upload

Sends file contents to a Notion upload.

```
PUT https://connect.mindcloud.co/v1/universal/notion/latest/actions/send-file-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/notion/latest/actions/send-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "fileUploadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notion/latest/actions/send-file-upload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "fileUploadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | File content to upload. |
| `fileUploadId` | string | yes | ID of the file upload to send data to. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `partNumber` | number | no | Part number for multipart uploads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | File upload identifier. |
| `object` | string | Returned object type. |
| `status` | string | Upload lifecycle status. |

## Native endpoint

Through the native Notion API, this operation is `POST /file_uploads/:file_upload_id/send` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-file-upload.md) for the provider-specific parameters and requirements.

