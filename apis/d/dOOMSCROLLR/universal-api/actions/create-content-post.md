# DOOMSCROLLR: Create Content Post



```
POST https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/create-content-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DOOMSCROLLR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/create-content-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/post"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/create-content-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/post"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the post content to publish in DOOMSCROLLR. Example: `https://example.com/post`. |
| `title` | string | no | Title of the content post. Example: `Post Title`. |
| `description` | string | no | Description text for the content post. Example: `Post description`. |
| `status` | string | no | Publish status for the new content post. Example: `published`. |
| `tags[]` | array<string> | no | Tags to associate with the content post. Accepts multiple values as an array. Example: `fashion,design,luxury`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DOOMSCROLLR API returns.

## Native endpoint

Through the native DOOMSCROLLR API, this operation is `POST /api/content/posts` (base URL `https://mindcloudapps0402.doomscrollr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-content-post.md) for the provider-specific parameters and requirements.

