# Eranol: Convert Image To WebP

Creates a WebP conversion job in Eranol.

```
POST https://connect.mindcloud.co/v1/universal/eranol/latest/actions/convert-image-to-webp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eranol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eranol/latest/actions/convert-image-to-webp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://raw.githubusercontent.com/mdn/dom-examples/main/canvas/pixel-manipulation/assets/rhino.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eranol/latest/actions/convert-image-to-webp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://raw.githubusercontent.com/mdn/dom-examples/main/canvas/pixel-manipulation/assets/rhino.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Image file URL to convert to WebP. Example: `https://raw.githubusercontent.com/mdn/dom-examples/main/canvas/pixel-manipulation/assets/rhino.jpg`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "jobType": "string",
      "message": "string",
      "resultUrl": "https://example.com",
      "status": "string",
      "statusUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Unique Eranol job identifier. |
| `jobType` | string | Provider job type label. |
| `message` | string | Provider status message. |
| `resultUrl` | string | URL for retrieving the completed job result. |
| `status` | string | Current job state. |
| `statusUrl` | string | URL for polling job status. |

## Native endpoint

Through the native Eranol API, this operation is `POST /ffmpeg/convert/image/to/webp` (base URL `https://eranol.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-image-to-webp.md) for the provider-specific parameters and requirements.

