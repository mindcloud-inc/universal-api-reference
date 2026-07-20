# RecurPost: Generate Image with AI

Generates an image with AI in RecurPost.

```
POST https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/generate-image-with-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RecurPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/generate-image-with-ai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "promptText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/generate-image-with-ai', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "promptText": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `promptText` | string | yes | Detailed description of the image to generate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "image_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `image_url` | string |  |

## Native endpoint

Through the native RecurPost API, this operation is `POST /api/generate_image_with_ai` (base URL `https://social.recurpost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image-with-ai.md) for the provider-specific parameters and requirements.

