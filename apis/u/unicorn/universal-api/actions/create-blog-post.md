# Unicorn: Create Blog Post

Creates a blog post in Unicorn.

```
POST https://connect.mindcloud.co/v1/universal/unicorn/latest/actions/create-blog-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unicorn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unicorn/latest/actions/create-blog-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "seobotPostId": "post-001",
  "slug": "launch-day",
  "html": "<p>Hello world</p>",
  "headline": "Launch Day",
  "metaDescription": "Announcing our new release.",
  "metaKeywords": "launch,release",
  "thumbnailUrl": "https://example.com/cover.png",
  "createdAt": "2026-04-06T10:00:00",
  "published": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unicorn/latest/actions/create-blog-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "seobotPostId": "post-001",
    "slug": "launch-day",
    "html": "<p>Hello world</p>",
    "headline": "Launch Day",
    "metaDescription": "Announcing our new release.",
    "metaKeywords": "launch,release",
    "thumbnailUrl": "https://example.com/cover.png",
    "createdAt": "2026-04-06T10:00:00",
    "published": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `seobotPostId` | string | yes | A string identifier that is unique across all Unicorn blog posts. Example: `post-001`. |
| `slug` | string | yes | Path of the new blog post. Must be unique across the blog. Example: `launch-day`. |
| `html` | string | yes | HTML content of the new post. Example: `<p>Hello world</p>`. |
| `headline` | string | yes | Meta title. Example: `Launch Day`. |
| `metaDescription` | string | yes | Meta description. Example: `Announcing our new release.`. |
| `metaKeywords` | string | yes | Meta keywords. Unicorn notes that these are not used anywhere at the moment. Example: `launch,release`. |
| `thumbnailUrl` | string | yes | Source URL of the post's thumbnail image. Example: `https://example.com/cover.png`. |
| `createdAt` | string | yes | Publication date in YYYY-MM-DDTHH:MM:SS format. Example: `2026-04-06T10:00:00`. |
| `published` | boolean | yes | Whether the new post is publicly available. Example: `true`. |
| `directory` | string | no | Optional subdirectory for the new blog post, for example nocode. Example: `nocode`. |
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
| `success` | boolean | Whether the blog post was created successfully. |

## Native endpoint

Through the native Unicorn API, this operation is `POST /blog_posts/seobot_hook/:seobot_api_key/:seobot_post_id` (base URL `https://api.unicornplatform.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-blog-post.md) for the provider-specific parameters and requirements.

