# Stability AI: Outpaint Image

Updates an image in Stability AI with outpainting.

```
PUT https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/outpaint-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stability AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/outpaint-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/outpaint-image', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image` | file | yes | Source image file to outpaint. |

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
| `finish_reason` | string | Reason the generation finished. |
| `image` | string | Generated image encoded as base64. |
| `seed` | number | Seed used for the generation. |

## Native endpoint

Through the native Stability AI API, this operation is `POST /v2beta/stable-image/edit/outpaint` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/outpaint-image.md) for the provider-specific parameters and requirements.

