# DeepImage: Resize to Exact Dimensions

Creates a resized image to exact dimensions in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/resize-to-exact-dimensions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/resize-to-exact-dimensions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "width": 1,
  "height": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/resize-to-exact-dimensions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "width": 1,
    "height": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the source image to resize. |
| `width` | number | yes | Exact output width in pixels. |
| `height` | number | yes | Exact output height in pixels. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": "string",
      "queue": 1,
      "resultUrl": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job` | string |  |
| `queue` | number |  |
| `resultUrl` | string |  |
| `status` | string |  |

## Native endpoint

Through the native DeepImage API, this operation is `POST /rest_api/process_result` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resize-to-exact-dimensions.md) for the provider-specific parameters and requirements.

