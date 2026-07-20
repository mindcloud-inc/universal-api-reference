# APImage: Analyze Image

Extracts text from an image with APImage.

```
POST https://connect.mindcloud.co/v1/universal/aPImage/latest/actions/analyze-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a APImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aPImage/latest/actions/analyze-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image_url": "https://example.com/image.png",
  "prompt": "List the objects and text visible in the image."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aPImage/latest/actions/analyze-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image_url": "https://example.com/image.png",
    "prompt": "List the objects and text visible in the image."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image_url` | string | yes | URL of the image to analyze. Example: `https://example.com/image.png`. |
| `prompt` | string | yes | Instruction for what to extract or describe from the image. Example: `List the objects and text visible in the image.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native APImage API returns.

## Native endpoint

Through the native APImage API, this operation is `POST /ai-image-to-text` (base URL `https://apimage.org/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-image.md) for the provider-specific parameters and requirements.

