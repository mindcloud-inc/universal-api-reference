# Stable Diffusion: Generate XL Image

Generates an XL image in Stable Diffusion.

```
POST https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/generate-xl-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stable Diffusion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/generate-xl-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text_prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/generate-xl-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text_prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text_prompt` | string | yes | Primary text prompt for image generation. |

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

Through the native Stable Diffusion API, this operation is `POST /v1/generation/stable-diffusion-xl-1024-v1-0/text-to-image` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-xl-image.md) for the provider-specific parameters and requirements.

