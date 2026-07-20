# DeepImage: Face Swap

Creates a face-swapped image in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/face-swap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/face-swap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://deep-image.ai/api-example3.jpg",
  "background.generate.ip_image2": "https://deep-image.ai/api-example3.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/face-swap', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://deep-image.ai/api-example3.jpg",
    "background.generate.ip_image2": "https://deep-image.ai/api-example3.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the original image whose face should be replaced. Example: `https://deep-image.ai/api-example3.jpg`. |
| `background.generate.ip_image2` | string | yes | Public URL of the face image that will be swapped into the source image. Example: `https://deep-image.ai/api-example3.jpg`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `background.generate.description` | string | no | Optional prompt used to creatively reimagine the swapped result. Example: `A cinematic scene with dramatic lighting, rich atmosphere, and dynamic composition.`. |
| `background.generate.strength` | number | no | Controls how strongly the result is reimagined during face swap. Default: `0.1`. |

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

Through the native DeepImage API, this operation is `POST /rest_api/process` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/face-swap.md) for the provider-specific parameters and requirements.

