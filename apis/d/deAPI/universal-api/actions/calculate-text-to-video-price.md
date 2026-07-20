# deAPI: Calculate Text-to-Video Price

Calculates text-to-video request pricing in deAPI.

```
GET https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/calculate-text-to-video-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a deAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/calculate-text-to-video-price?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/calculate-text-to-video-price?${params}`, {
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
| `fps` | string | no | Frames per second for pricing. |
| `frames` | string | no | Number of frames to price. |
| `height` | string | no | Video height in pixels. |
| `model` | string | no | Video model slug from List Models. |
| `steps` | string | no | Number of inference steps. |
| `width` | string | no | Video width in pixels. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native deAPI API returns.

## Native endpoint

Through the native deAPI API, this operation is `POST /api/v1/client/txt2video/price-calculation` (base URL `https://api.deapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-text-to-video-price.md) for the provider-specific parameters and requirements.

