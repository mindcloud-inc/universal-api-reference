# DeepAI: Creative Upscale

Creates a creatively upscaled image in DeepAI.

```
POST https://connect.mindcloud.co/v1/universal/deepAI/latest/actions/creative-upscale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepAI/latest/actions/creative-upscale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "https://example.com/image.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepAI/latest/actions/creative-upscale', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image": "https://example.com/image.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image` | string | yes | The image URL or uploaded file to upscale creatively. Example: `https://example.com/image.jpg`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DeepAI API returns.

## Native endpoint

Through the native DeepAI API, this operation is `POST /creative-upscale` (base URL `https://api.deepai.org/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/creative-upscale.md) for the provider-specific parameters and requirements.

