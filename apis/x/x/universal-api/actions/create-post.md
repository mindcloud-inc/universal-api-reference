# X: Create Post



```
POST https://connect.mindcloud.co/v1/universal/x/latest/actions/create-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/x/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/x/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | no | The text of your post (up to 280 characters). |
| `media.media_ids[]` | array<string> | no | Array of media IDs (from the Upload Media action) to attach to the post. Max 4 images or 1 video/GIF. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native X API returns.

## Native endpoint

Through the native X API, this operation is `POST /2/tweets` (base URL `https://api.x.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post.md) for the provider-specific parameters and requirements.

