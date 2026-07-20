# Recut URL Shortener: Upload File

Uploads a file to Recut URL Shortener.

```
POST https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "report.csv",
  "fileData": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "report.csv",
    "fileData": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | File name including extension to place in the upload URL Example: `report.csv`. |
| `fileData` | file | yes | Binary file data to send as the raw request body |
| `name` | string | no | Display name for the uploaded file Example: `MindCloud Upload`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `custom` | string | no | Custom alias instead of random alias Example: `mindcloud-report`. |
| `domain` | string | no | Custom domain Example: `https://go.example.com`. |
| `password` | string | no | Password protection Example: `secret123`. |
| `expiry` | date | no | Expiration date such as 2021-09-28 Example: `2026-05-01`. |
| `maxDownloads` | number | no | Maximum number of downloads Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "0": "string",
      "1": 1,
      "error": true,
      "shorturl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `0` | string |  |
| `1` | number |  |
| `error` | boolean |  |
| `shorturl` | string |  |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `POST /files/upload/:filename` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

