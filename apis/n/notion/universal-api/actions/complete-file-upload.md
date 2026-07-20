# Notion: Complete File Upload

Finalizes a file upload in Notion.

```
PUT https://connect.mindcloud.co/v1/universal/notion/latest/actions/complete-file-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/notion/latest/actions/complete-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileUploadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notion/latest/actions/complete-file-upload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileUploadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUploadId` | string | yes | ID of the file upload to complete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiryTime": "2026-05-07T12:00:00.000Z",
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
| `expiryTime` | date | Upload expiry timestamp. |
| `id` | string | File upload identifier. |
| `object` | string | Returned object type. |
| `status` | string | Upload lifecycle status. |

## Native endpoint

Through the native Notion API, this operation is `POST /file_uploads/:file_upload_id/complete` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-file-upload.md) for the provider-specific parameters and requirements.

