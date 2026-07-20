# Stable Diffusion: Get Creative Upscale Result

Retrieves a creative upscale result from Stable Diffusion.

```
GET https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/get-creative-upscale-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stable Diffusion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/get-creative-upscale-result?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/get-creative-upscale-result?${params}`, {
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
| `id` | string | yes | Generation identifier returned by creative upscale. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finish_reason": "string",
      "id": "string",
      "image": "string",
      "seed": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finish_reason` | string |  |
| `id` | string |  |
| `image` | string |  |
| `seed` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Stable Diffusion API, this operation is `GET /v2beta/stable-image/upscale/creative/result/{id}` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-creative-upscale-result.md) for the provider-specific parameters and requirements.

