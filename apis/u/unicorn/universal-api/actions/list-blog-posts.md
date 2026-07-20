# Unicorn: List Blog Posts

Retrieves published blog posts from Unicorn.

```
GET https://connect.mindcloud.co/v1/universal/unicorn/latest/actions/list-blog-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unicorn `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subdomain` | string | yes | The default subdomain of your Unicorn blog website. Example: `your-blog-subdomain`. |
| `amount` | number | no | The number of posts to return. Example: `10`. |
| `excludePostContent` | boolean | no | Exclude the post body fields from the response when true. Example: `false`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author_id` | number |  |
| `blog` | number |  |
| `blog_url` | string |  |
| `body_html` | string |  |
| `body_json` | object |  |
| `comments` | object |  |
| `created` | string |  |
| `custom_head_html_code` | string |  |
| `directory` | string |  |
| `displayed_thumbnail` | string |  |
| `editor_type` | string |  |
| `excerpt` | string |  |
| `filters` | object |  |
| `first_image_height` | number |  |
| `first_image_url` | string |  |
| `first_image_width` | number |  |
| `first_paragraph_text` | string |  |
| `id` | number |  |
| `is_deleted` | boolean |  |
| `is_locked` | boolean |  |
| `is_meta_description_inherited` | boolean |  |
| `is_meta_keywords_inherited` | boolean |  |
| `is_seobot_post` | boolean |  |
| `likes` | number |  |
| `meta_description` | string |  |
| `meta_keywords` | string |  |
| `meta_title` | string |  |
| `modified` | string |  |
| `og_description` | string |  |
| `og_image_height` | number |  |
| `og_image_url` | string |  |
| `og_image_uuid` | string |  |
| `og_image_width` | number |  |
| `og_title` | string |  |
| `published_on` | string |  |
| `shares` | object |  |
| `status` | string |  |
| `thumbnail_alt` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Unicorn API, this operation is `GET /blog_posts/get_posts/:subdomain` (base URL `https://api.unicornplatform.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-blog-posts.md) for the provider-specific parameters and requirements.

