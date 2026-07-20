# DeepImage: Inpainting / Outpainting

Creates an inpainted or outpainted image in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/inpainting-outpainting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/inpainting-outpainting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://deep-image.ai/api-example2.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/inpainting-outpainting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://deep-image.ai/api-example2.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the source image to edit or expand. Example: `https://deep-image.ai/api-example2.jpg`. |
| `background.generate.adapter_type` | string | no | Use `inpainting` for masked edits or `upscale` when pairing prompt guidance with outpainting. Example: `inpainting`. |
| `background.generate.description` | string | no | Prompt for the fill or uncrop result. Example: `Boat on Mars with spaceships around.`. |
| `width` | number | no | Target width used for uncrop/outpainting workflows. Default: `2000`. |
| `height` | number | no | Target height used for uncrop/outpainting workflows. Default: `1000`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `background.generate.ip_image2` | string | no | Public URL of the mask image used for inpainting. Example: `https://s3.eu-central-1.amazonaws.com/deep-image.ai/api-examples/inpainting-example-mask4.png`. |
| `background.generate.controlnet_conditioning_scale` | number | no | DeepImage conditioning scale for inpainting masks. Default: `0.5`. |
| `fit.canvas` | string | no | Canvas expansion mode used for outpainting. Default: `outpainting`. |

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

Through the native DeepImage API, this operation is `POST /rest_api/process` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/inpainting-outpainting.md) for the provider-specific parameters and requirements.

