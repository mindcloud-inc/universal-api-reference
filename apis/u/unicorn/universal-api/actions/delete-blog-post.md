# Unicorn: Delete Blog Post

Deletes an existing blog post from Unicorn.

```
DELETE https://connect.mindcloud.co/v1/universal/unicorn/latest/actions/delete-blog-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unicorn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/unicorn/latest/actions/delete-blog-post?connectionId=$CONNECTION_ID&seobotPostId=post-001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "seobotPostId": "post-001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unicorn/latest/actions/delete-blog-post?${params}`, {
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
| `seobotPostId` | string | yes | The unique string identifier assigned when the post was created. Example: `post-001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "new_url": "https://example.com",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `new_url` | string | The new URL returned by Unicorn after the delete completes. |
| `success` | boolean | Whether the blog post was deleted successfully. |

## Native endpoint

Through the native Unicorn API, this operation is `DELETE /blog_posts/seobot_hook/:seobot_api_key/:seobot_post_id` (base URL `https://api.unicornplatform.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-blog-post.md) for the provider-specific parameters and requirements.

