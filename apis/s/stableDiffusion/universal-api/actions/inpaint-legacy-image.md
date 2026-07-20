# Stable Diffusion: Inpaint Legacy Image

Inpaints an image with the legacy Stable Diffusion endpoint.

```
POST https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/inpaint-legacy-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stable Diffusion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/inpaint-legacy-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "string",
  "mode": "search",
  "prompt": "string",
  "search_prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/inpaint-legacy-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image": "string",
    "mode": "search",
    "prompt": "string",
    "search_prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image` | string | yes | Source image to inpaint. |
| `mode` | string | yes | Inpainting mode. Use search for prompt-guided region selection. Default: `search`. |
| `prompt` | string | yes | Text prompt describing the desired inpainted output. |
| `search_prompt` | string | yes | Short description of the region or object to replace when using search mode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finish_reason": "string",
      "image": "string",
      "seed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finish_reason` | string |  |
| `image` | string |  |
| `seed` | number |  |

## Native endpoint

Through the native Stable Diffusion API, this operation is `POST /v2alpha/generation/stable-image/inpaint` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/inpaint-legacy-image.md) for the provider-specific parameters and requirements.

