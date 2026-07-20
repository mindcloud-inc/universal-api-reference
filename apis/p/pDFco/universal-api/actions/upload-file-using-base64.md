# PDF.co: Upload File Using Base64

Uploads a file from Base64 to PDF.co.

```
POST https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/upload-file-using-base64
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/upload-file-using-base64" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/upload-file-using-base64', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | yes | Base64-encoded file content. |
| `name` | string | no | Filename to use for uploaded content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expiration` | number | no | Optional temporary file expiration in minutes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": 1,
      "duration": 1,
      "error": true,
      "name": "Ava Chen",
      "outputLinkValidTill": "2026-05-07T12:00:00.000Z",
      "remainingCredits": 1,
      "status": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number | Credits consumed by this call. |
| `duration` | number | Processing duration in ms. |
| `error` | boolean | Whether the request failed. |
| `name` | string | Stored temporary filename. |
| `outputLinkValidTill` | date | Expiration timestamp for the temporary URL. |
| `remainingCredits` | number | Credits left in the account. |
| `status` | number | HTTP-like status code from PDF.co. |
| `url` | string | Temporary PDF.co URL for the uploaded file. |

## Native endpoint

Through the native PDF.co API, this operation is `POST /file/upload/base64` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-using-base64.md) for the provider-specific parameters and requirements.

