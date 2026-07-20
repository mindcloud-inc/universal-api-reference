# Higgsfield AI: Generate File Upload URL



```
POST https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/generate-file-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Higgsfield AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/generate-file-upload-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/generate-file-upload-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentType` | string | no | MIME type for the file to upload, for example image/jpeg. Default: `image/jpeg`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content_type": "string",
      "public_url": "https://example.com",
      "upload_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content_type` | string |  |
| `public_url` | string |  |
| `upload_url` | string |  |

## Native endpoint

Through the native Higgsfield AI API, this operation is `POST /files/generate-upload-url` (base URL `https://platform.higgsfield.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-file-upload-url.md) for the provider-specific parameters and requirements.

