# Unicorn: Update Blog Post

Updates an existing blog post in Unicorn.

```
PUT https://connect.mindcloud.co/v1/universal/unicorn/latest/actions/update-blog-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unicorn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unicorn/latest/actions/update-blog-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "seobotPostId": "post-001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unicorn/latest/actions/update-blog-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "seobotPostId": "post-001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `seobotPostId` | string | yes | The unique string identifier assigned when the post was created. Example: `post-001`. |
| `slug` | string | no | Path of the updated blog post. Must be unique across the blog when changed. Example: `launch-day`. |
| `html` | string | no | HTML content of the updated post. Example: `<p>Updated post</p>`. |
| `headline` | string | no | Meta title. Example: `Updated title`. |
| `metaDescription` | string | no | Meta description. Example: `Updated description`. |
| `metaKeywords` | string | no | Meta keywords. Unicorn notes that these are not used anywhere at the moment. Example: `updated,keywords`. |
| `thumbnailUrl` | string | no | Source URL of the post's thumbnail image. Example: `https://example.com/updated-cover.png`. |
| `createdAt` | string | no | Publication date in YYYY-MM-DDTHH:MM:SS format. Example: `2026-04-06T10:00:00`. |
| `published` | boolean | no | Whether the updated post is publicly available. Example: `true`. |
| `directory` | string | no | Optional subdirectory for the blog post, for example nocode. Example: `nocode`. |
| `isDeleted` | boolean | no | Mark the post as deleted. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the blog post was updated successfully. |

## Native endpoint

Through the native Unicorn API, this operation is `PATCH /blog_posts/seobot_hook/:seobot_api_key/:seobot_post_id` (base URL `https://api.unicornplatform.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-blog-post.md) for the provider-specific parameters and requirements.

