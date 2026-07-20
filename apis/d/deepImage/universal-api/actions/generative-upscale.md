# DeepImage: Generative Upscale

Creates a generatively upscaled image in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/generative-upscale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/generative-upscale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://deep-image.ai/api-example.png",
  "width": "3000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/generative-upscale', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://deep-image.ai/api-example.png",
    "width": "3000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the image to upscale. Example: `https://deep-image.ai/api-example.png`. |
| `width` | number | yes | Desired output width in pixels. Default: `3000`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `height` | number | no | Optional output height in pixels when you want to force exact dimensions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageApp": "string",
      "job": "string",
      "originalImg": "string",
      "queue": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageApp` | string |  |
| `job` | string |  |
| `originalImg` | string |  |
| `queue` | number |  |

## Native endpoint

Through the native DeepImage API, this operation is `POST /rest_api/process` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generative-upscale.md) for the provider-specific parameters and requirements.

