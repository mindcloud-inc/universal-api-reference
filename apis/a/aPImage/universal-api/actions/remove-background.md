# APImage: Remove Background

Removes the background from an image with APImage.

```
POST https://connect.mindcloud.co/v1/universal/aPImage/latest/actions/remove-background
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a APImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aPImage/latest/actions/remove-background" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input_image": "https://example.com/image.png",
  "prompt": "remove background"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aPImage/latest/actions/remove-background', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input_image": "https://example.com/image.png",
    "prompt": "remove background"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input_image` | string | yes | Source image URL to process for background removal. Example: `https://example.com/image.png`. |
| `prompt` | string | yes | Include a phrase like 'remove background' to trigger the background-removal flow. Example: `remove background`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native APImage API returns.

## Native endpoint

Through the native APImage API, this operation is `POST https://app.apimage.org/api/v1/image-studio` (base URL `https://apimage.org/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-background.md) for the provider-specific parameters and requirements.

