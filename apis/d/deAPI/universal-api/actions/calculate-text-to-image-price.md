# deAPI: Calculate Text-to-Image Price

Calculates text-to-image request pricing in deAPI.

```
GET https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/calculate-text-to-image-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a deAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/calculate-text-to-image-price?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/calculate-text-to-image-price?${params}`, {
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
| `guidance` | string | no | Guidance scale for estimation. |
| `height` | string | no | Image height in pixels. |
| `model` | string | no | Image model slug from List Models. |
| `negativePrompt` | string | no | Elements to avoid in the generated image. |
| `prompt` | string | no | Main prompt for image price estimation. |
| `seed` | string | no | Random seed for estimation. |
| `steps` | string | no | Number of inference steps. |
| `width` | string | no | Image width in pixels. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native deAPI API returns.

## Native endpoint

Through the native deAPI API, this operation is `POST /api/v1/client/txt2img/price-calculation` (base URL `https://api.deapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-text-to-image-price.md) for the provider-specific parameters and requirements.

