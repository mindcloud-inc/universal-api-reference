# Unicorn Universal API Examples

These examples use the MindCloud API key and Unicorn connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Blog Posts

Retrieves published blog posts from Unicorn.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unicorn/latest/actions/list-blog-posts?connectionId=$CONNECTION_ID&subdomain=your-blog-subdomain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subdomain": "your-blog-subdomain"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unicorn/latest/actions/list-blog-posts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "author_id": 1,
      "blog": 1,
      "blog_url": "https://example.com",
      "body_html": "string",
      "body_json": {},
      "comments": {},
      "created": "string",
      "custom_head_html_code": "string",
      "directory": "string",
      "displayed_thumbnail": "string",
      "editor_type": "string",
      "excerpt": "string",
      "filters": {},
      "first_image_height": 1,
      "first_image_url": "https://example.com",
      "first_image_width": 1,
      "first_paragraph_text": "string",
      "id": 1,
      "is_deleted": true,
      "is_locked": true,
      "is_meta_description_inherited": true,
      "is_meta_keywords_inherited": true,
      "is_seobot_post": true,
      "likes": 1,
      "meta_description": "string",
      "meta_keywords": "string",
      "meta_title": "string",
      "modified": "string",
      "og_description": "string",
      "og_image_height": 1,
      "og_image_url": "https://example.com",
      "og_image_uuid": "string",
      "og_image_width": 1,
      "og_title": "string",
      "published_on": "string",
      "shares": {},
      "status": "string",
      "thumbnail_alt": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Blog Posts action reference](actions/list-blog-posts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/unicorn/latest/actions/list-blog-posts).

## Create Blog Post

Creates a blog post in Unicorn.

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

Example response:

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

See the full [Create Blog Post action reference](actions/create-blog-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/unicorn/latest/actions/create-blog-post).
