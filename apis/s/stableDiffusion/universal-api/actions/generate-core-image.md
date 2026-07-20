# Stable Diffusion: Generate Core Image

Generates an image with Stable Diffusion Core.

```
POST https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/generate-core-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stable Diffusion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/generate-core-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/generate-core-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | Text prompt describing the image to generate. |

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

Through the native Stable Diffusion API, this operation is `POST /v2beta/stable-image/generate/core` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-core-image.md) for the provider-specific parameters and requirements.

