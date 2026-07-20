# Stability AI: Remove Image Background

Removes an image background in Stability AI.

```
POST https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/remove-image-background
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stability AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/remove-image-background" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/remove-image-background', {
  method: 'POST',
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
| `image` | file | yes | Source image file whose background should be removed. |

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

Through the native Stability AI API, this operation is `POST /v2beta/stable-image/edit/remove-background` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-image-background.md) for the provider-specific parameters and requirements.

