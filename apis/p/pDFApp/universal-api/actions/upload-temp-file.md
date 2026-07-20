# PDF-app: Upload Temp File

Creates temporary file URLs in PDF-app.

```
POST https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/upload-temp-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/upload-temp-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/upload-temp-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileUrls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUrls[]` | array<string> | yes | Public file URLs to upload into PDF-app temporary storage. |
| `operationType` | string | no | Optional upload mode such as zip, upload, or download. |
| `fileType` | string | no | File type used when requesting a presigned upload URL. |
| `filePath` | string | no | Stored upload path used when requesting a presigned download URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditzConsumed": 1,
      "creditzRemaining": 1,
      "jobId": "string",
      "message": "string",
      "presignedUrls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditzConsumed` | number |  |
| `creditzRemaining` | number |  |
| `jobId` | string |  |
| `message` | string |  |
| `presignedUrls[]` | string |  |

## Native endpoint

Through the native PDF-app API, this operation is `POST /uploadtempFile` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-temp-file.md) for the provider-specific parameters and requirements.

