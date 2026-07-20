# DeepAI: Replace Image Region

Creates an edited image by replacing a masked region in DeepAI.

```
POST https://connect.mindcloud.co/v1/universal/deepAI/latest/actions/replace-image-region
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepAI/latest/actions/replace-image-region" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "Replace the masked area with a mountain lake",
  "mask": "https://example.com/mask.png",
  "image": "https://example.com/image.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepAI/latest/actions/replace-image-region', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "Replace the masked area with a mountain lake",
    "mask": "https://example.com/mask.png",
    "image": "https://example.com/image.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | The prompt describing what should replace the masked region. Example: `Replace the masked area with a mountain lake`. |
| `mask` | string | yes | The image URL or uploaded mask file identifying the region to replace. Example: `https://example.com/mask.png`. |
| `image` | string | yes | The source image URL or uploaded file to modify. Example: `https://example.com/image.jpg`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DeepAI API returns.

## Native endpoint

Through the native DeepAI API, this operation is `POST /image-replace` (base URL `https://api.deepai.org/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-image-region.md) for the provider-specific parameters and requirements.

