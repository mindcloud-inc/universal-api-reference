# Olostep: Complete File Upload

Completes a file upload in Olostep.

```
PUT https://connect.mindcloud.co/v1/universal/olostep/latest/actions/complete-file-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/complete-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "file_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/olostep/latest/actions/complete-file-upload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "file_123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | The ID of the uploaded file to finalize. Example: `file_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bytes": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "id": "string",
      "object": "string",
      "purpose": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bytes` | number | The uploaded file size in bytes. |
| `created` | date | Unix timestamp when the file was created. |
| `filename` | string | The uploaded filename. |
| `id` | string | The file ID. |
| `object` | string | The returned object type. |
| `purpose` | string | The file purpose. |
| `status` | string | The file processing status. |

## Native endpoint

Through the native Olostep API, this operation is `POST /v1/files/[:file_id]/complete` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-file-upload.md) for the provider-specific parameters and requirements.

