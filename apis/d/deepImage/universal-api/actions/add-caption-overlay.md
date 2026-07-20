# DeepImage: Add Caption Overlay

Creates an image with caption overlay in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/add-caption-overlay
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/add-caption-overlay" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "caption.url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/add-caption-overlay', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "caption.url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the source image to caption. |
| `caption.url` | string | yes | Public URL of the overlay image to place on top of the result. |
| `caption.position` | string | no | Caption position such as RB, LT, or MM. Default: `RB`. |
| `caption.target_width_percentage` | number | no | Caption width as a percentage of the destination image width. Default: `25`. |
| `caption.padding` | number | no | Padding in pixels between the caption and the image border. |
| `caption.opacity` | number | no | Caption opacity from 0 to 100. Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": "string",
      "queue": 1,
      "result_url": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job` | string | DeepImage processing job identifier. |
| `queue` | number | Queue position when DeepImage reports it. |
| `result_url` | string | URL of the processed image when available. |
| `status` | string | Processing status returned by DeepImage. |

## Native endpoint

Through the native DeepImage API, this operation is `POST /rest_api/process_result` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-caption-overlay.md) for the provider-specific parameters and requirements.

