# Baserow: Upload File Via URL

Uploads a file to Baserow from a URL.

```
POST https://connect.mindcloud.co/v1/universal/baserow/latest/actions/upload-file-via-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baserow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/upload-file-via-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baserow/latest/actions/upload-file-via-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The public file URL that Baserow should download and upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageHeight": {},
      "imageWidth": {},
      "isImage": true,
      "mimeType": "string",
      "name": "Ava Chen",
      "originalName": "Ava Chen",
      "size": 1,
      "thumbnails": {},
      "uploadedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageHeight` | object |  |
| `imageWidth` | object |  |
| `isImage` | boolean |  |
| `mimeType` | string |  |
| `name` | string |  |
| `originalName` | string |  |
| `size` | number |  |
| `thumbnails` | object |  |
| `uploadedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Baserow API, this operation is `POST /api/user-files/upload-via-url/` (base URL `https://api.baserow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-via-url.md) for the provider-specific parameters and requirements.

