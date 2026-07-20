# TimelinesAI: Upload File by URL

Creates a TimelinesAI file from a public URL.

```
POST https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/upload-file-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/upload-file-by-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "downloadUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/upload-file-by-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "downloadUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `downloadUrl` | string | yes | Publicly accessible URL of the file to upload. |
| `filename` | string | no | Optional filename to store for the uploaded file. |
| `contentType` | string | no | Optional MIME type for the uploaded file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "filename": "Ava Chen",
        "mimetype": "string",
        "size": 1,
        "temporaryDownloadUrl": "https://example.com",
        "uid": "string",
        "uploadedAt": "string",
        "uploadedByEmail": "ava@example.com"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.filename` | string |  |
| `data.mimetype` | string |  |
| `data.size` | number |  |
| `data.temporaryDownloadUrl` | string |  |
| `data.uid` | string |  |
| `data.uploadedAt` | string |  |
| `data.uploadedByEmail` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `POST /files` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-by-url.md) for the provider-specific parameters and requirements.

