# Notion: Create File Upload

Initiates a new file upload in Notion.

```
POST https://connect.mindcloud.co/v1/universal/notion/latest/actions/create-file-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notion/latest/actions/create-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen",
  "contentType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notion/latest/actions/create-file-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen",
    "contentType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | Name of the file to upload. |
| `mode` | string | no | Upload mode: single_part or multi_part. |
| `contentType` | string | yes | MIME content type of the file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `numberOfParts` | number | no | Number of upload parts for multi-part upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiryTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "object": "string",
      "status": "string",
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiryTime` | date | Upload URL expiry timestamp. |
| `id` | string | File upload identifier. |
| `object` | string | Returned object type. |
| `status` | string | Upload lifecycle status. |
| `uploadUrl` | string | Pre-signed URL for sending content. |

## Native endpoint

Through the native Notion API, this operation is `POST /file_uploads` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file-upload.md) for the provider-specific parameters and requirements.

