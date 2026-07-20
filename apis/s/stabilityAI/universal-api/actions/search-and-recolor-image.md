# Stability AI: Search And Recolor Image

Updates an image in Stability AI by search and recolor.

```
PUT https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/search-and-recolor-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stability AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/search-and-recolor-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "string",
  "prompt": "string",
  "selectPrompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/search-and-recolor-image', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image": "string",
    "prompt": "string",
    "selectPrompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image` | file | yes | Source image file to edit. |
| `prompt` | string | yes | Prompt describing the desired color or visual change. |
| `selectPrompt` | string | yes | Description of the object or region to select for recoloring. |

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

Through the native Stability AI API, this operation is `POST /v2beta/stable-image/edit/search-and-recolor` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-and-recolor-image.md) for the provider-specific parameters and requirements.

