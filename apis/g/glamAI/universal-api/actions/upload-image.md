# Glam AI: Upload Image

Uploads an image to Glam AI.

```
POST https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/upload-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Glam AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/upload-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/upload-image', {
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
| `file` | file | yes | Image file to upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file_url` | string | Public URL of the uploaded image. |

## Native endpoint

Through the native Glam AI API, this operation is `POST /upload` (base URL `https://api.glam.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-image.md) for the provider-specific parameters and requirements.

