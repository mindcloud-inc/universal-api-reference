# DeepImage: Text-to-Image Generation

Creates an image from text in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/text-to-image-generation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/text-to-image-generation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "background.generate.description": "woman in a futuristic suit holding a gun in her hand, looking at the camera, cyberpunk art, neo-figurative, anime"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/text-to-image-generation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "background.generate.description": "woman in a futuristic suit holding a gun in her hand, looking at the camera, cyberpunk art, neo-figurative, anime"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `background.generate.description` | string | yes | Prompt describing the image to generate. Example: `woman in a futuristic suit holding a gun in her hand, looking at the camera, cyberpunk art, neo-figurative, anime`. |
| `width` | number | no | Target width of the generated image. Default: `2048`. |
| `height` | number | no | Target height of the generated image. Default: `1024`. |

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

Through the native DeepImage API, this operation is `POST /rest_api/process` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/text-to-image-generation.md) for the provider-specific parameters and requirements.

