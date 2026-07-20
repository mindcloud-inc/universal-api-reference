# Stable Diffusion: Mask XL Image

Masks an XL image in Stable Diffusion.

```
POST https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/mask-xl-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stable Diffusion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/mask-xl-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "init_image": "string",
  "mask_source": "string",
  "text_prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/mask-xl-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "init_image": "string",
    "mask_source": "string",
    "text_prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `init_image` | string | yes | Source image to transform. |
| `mask_source` | string | yes | Masking strategy to use for the source image. |
| `text_prompt` | string | yes | Primary text prompt for the masked image generation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "artifacts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `artifacts` | array<object> |  |

## Native endpoint

Through the native Stable Diffusion API, this operation is `POST /v1/generation/stable-diffusion-xl-1024-v1-0/image-to-image/masking` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mask-xl-image.md) for the provider-specific parameters and requirements.

