# ContentStudio: Create Post

Creates a new social media post in ContentStudio.

```
POST https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/create-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContentStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accounts[]": [
    "string"
  ],
  "content": {},
  "scheduling": {},
  "workspace_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accounts[]": ["string"],
    "content": {},
    "scheduling": {},
    "workspace_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accounts[]` | array<string> | yes | Account IDs to post to. |
| `approval` | object | no | Optional approval workflow payload. |
| `campaign_id` | string | no | Optional campaign ID. |
| `content` | object | yes | Post content payload. |
| `content_category_id` | string | no | Optional content category ID. |
| `first_comment` | object | no | Optional first comment payload. |
| `gmb_options` | object | no | Optional Google Business Profile options. |
| `labels[]` | array<string> | no | Optional label IDs. |
| `pinterest_options` | object | no | Optional Pinterest options. |
| `post_type` | string | no | Optional post type. |
| `post_video_title` | string | no | Optional video title. |
| `scheduling` | object | yes | Scheduling payload. |
| `tiktok_options` | object | no | Optional TikTok options. |
| `workspace_id` | string | yes | ContentStudio workspace ID. |
| `youtube_options` | object | no | Optional YouTube options. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "postUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `postUrl` | string |  |

## Native endpoint

Through the native ContentStudio API, this operation is `POST /workspaces/:workspace_id/posts` (base URL `https://api.contentstudio.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post.md) for the provider-specific parameters and requirements.

