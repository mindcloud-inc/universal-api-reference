# Grok: Initialize File Upload

Creates a chunked file upload session in Grok.

```
POST https://connect.mindcloud.co/v1/universal/grok/latest/actions/initialize-file-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grok/latest/actions/initialize-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "contentType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/initialize-file-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "contentType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | File name to initialize. |
| `contentType` | string | yes | MIME content type for the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "createdAt": "string",
      "expiresAt": "string",
      "fileId": "string",
      "filePath": "string",
      "name": "Ava Chen",
      "processingStatus": "string",
      "sizeBytes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | Content type registered for the upload. |
| `createdAt` | string | Timestamp when the upload record was created. |
| `expiresAt` | string | Timestamp when the upload record expires. |
| `fileId` | string | Initialized upload identifier. |
| `filePath` | string | Provider file path or storage reference. |
| `name` | string | File name registered for the upload. |
| `processingStatus` | string | Current processing status for the upload. |
| `sizeBytes` | number | Expected file size in bytes. |

## Native endpoint

Through the native Grok API, this operation is `POST /v1/files:initialize` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initialize-file-upload.md) for the provider-specific parameters and requirements.

