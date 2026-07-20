# BulkSMS: Create Attachment Upload URL

Creates a signed BulkSMS attachment upload URL.

```
POST https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/create-attachment-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/create-attachment-upload-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileExtension": "string",
  "mediaType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/create-attachment-upload-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileExtension": "string",
    "mediaType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileExtension` | string | yes | File extension for the attachment upload, usually related to the media type. |
| `mediaType` | string | yes | Media type of the file to upload, such as application/pdf. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fetchUrl": "https://example.com",
      "fields": [
        {}
      ],
      "putUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fetchUrl` | string |  |
| `fields` | array<object> |  |
| `putUrl` | string |  |

## Native endpoint

Through the native BulkSMS API, this operation is `POST /rmm/pre-sign-attachment` (base URL `https://api.bulksms.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-attachment-upload-url.md) for the provider-specific parameters and requirements.

