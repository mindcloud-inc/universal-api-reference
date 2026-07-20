# Tumblr: Get User Limits

Retrieves Tumblr posting limits for the user.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-user-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-user-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-user-limits?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "user": {
        "blogs": {
          "description": "string",
          "limit": 1,
          "remaining": 1,
          "resetAt": 1
        },
        "communityPosts": {
          "description": "string",
          "limit": 1,
          "remaining": 1,
          "resetAt": 1
        },
        "follows": {
          "description": "string",
          "limit": 1,
          "remaining": 1,
          "resetAt": 1
        },
        "likes": {
          "description": "string",
          "limit": 1,
          "remaining": 1,
          "resetAt": 1
        },
        "photos": {
          "description": "string",
          "limit": 1,
          "remaining": 1,
          "resetAt": 1
        },
        "posts": {
          "description": "string",
          "limit": 1,
          "remaining": 1,
          "resetAt": 1
        },
        "replyLikes": {
          "description": "string",
          "limit": 1,
          "remaining": 1,
          "resetAt": 1
        },
        "videos": {
          "description": "string",
          "limit": 1,
          "remaining": 1,
          "resetAt": 1
        },
        "videoSeconds": {
          "description": "string",
          "limit": 1,
          "remaining": 1,
          "resetAt": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user.blogs.description` | string |  |
| `user.blogs.limit` | number |  |
| `user.blogs.remaining` | number |  |
| `user.blogs.resetAt` | number |  |
| `user.communityPosts.description` | string |  |
| `user.communityPosts.limit` | number |  |
| `user.communityPosts.remaining` | number |  |
| `user.communityPosts.resetAt` | number |  |
| `user.follows.description` | string |  |
| `user.follows.limit` | number |  |
| `user.follows.remaining` | number |  |
| `user.follows.resetAt` | number |  |
| `user.likes.description` | string |  |
| `user.likes.limit` | number |  |
| `user.likes.remaining` | number |  |
| `user.likes.resetAt` | number |  |
| `user.photos.description` | string |  |
| `user.photos.limit` | number |  |
| `user.photos.remaining` | number |  |
| `user.photos.resetAt` | number |  |
| `user.posts.description` | string |  |
| `user.posts.limit` | number |  |
| `user.posts.remaining` | number |  |
| `user.posts.resetAt` | number |  |
| `user.replyLikes.description` | string |  |
| `user.replyLikes.limit` | number |  |
| `user.replyLikes.remaining` | number |  |
| `user.replyLikes.resetAt` | number |  |
| `user.videos.description` | string |  |
| `user.videos.limit` | number |  |
| `user.videos.remaining` | number |  |
| `user.videos.resetAt` | number |  |
| `user.videoSeconds.description` | string |  |
| `user.videoSeconds.limit` | number |  |
| `user.videoSeconds.remaining` | number |  |
| `user.videoSeconds.resetAt` | number |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/user/limits` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-limits.md) for the provider-specific parameters and requirements.

