# VisionFly: Serve CDN Image

Retrieves an image from the VisionFly CDN.

```
GET https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/serve-cdn-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VisionFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/serve-cdn-image?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/serve-cdn-image?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | string | no | Output format such as webp, avif, png, jpeg, or auto. |
| `height` | string | no | Optional output height in pixels. |
| `imageId` | string | no | VisionFly image identifier. |
| `optimize` | string | no | Apply smart optimization. |
| `quality` | string | no | Output quality from 1 to 100. |
| `width` | string | no | Optional output width in pixels. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Binary image payload returned by the provider as a buffer wrapper. |
| `meta` | object | Execution metadata including HTTP response details. |
| `success` | boolean | Whether the CDN transform request succeeded. |

## Native endpoint

Through the native VisionFly API, this operation is `GET /cdn/:image_id` (base URL `https://api.visionfly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/serve-cdn-image.md) for the provider-specific parameters and requirements.

