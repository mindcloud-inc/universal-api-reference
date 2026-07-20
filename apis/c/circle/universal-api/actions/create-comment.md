# Circle: Create Comment

Creates a new comment in Circle.

```
POST https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string",
  "postId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string",
    "postId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | yes | Comment body content |
| `postId` | list<number> | yes | Post ID to attach comment to |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": {
        "body": "string",
        "createdAt": "string",
        "id": "string",
        "name": "Ava Chen",
        "recordId": 1,
        "recordType": "string",
        "updatedAt": "string"
      },
      "communityId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "flaggedForApprovalAt": "string",
      "id": 1,
      "likesCount": 1,
      "parentCommentId": "string",
      "post": {
        "id": 1,
        "name": "Ava Chen",
        "slug": "string"
      },
      "repliesCount": 1,
      "space": {
        "id": 1,
        "name": "Ava Chen",
        "slug": "string"
      },
      "url": "https://example.com",
      "user": {
        "avatarUrl": "https://example.com",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      },
      "userCommentsCount": 1,
      "userLikesCount": 1,
      "userPostsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body.body` | string |  |
| `body.createdAt` | string |  |
| `body.id` | string |  |
| `body.name` | string |  |
| `body.recordId` | number |  |
| `body.recordType` | string |  |
| `body.updatedAt` | string |  |
| `communityId` | number |  |
| `createdAt` | date |  |
| `flaggedForApprovalAt` | string |  |
| `id` | number |  |
| `likesCount` | number |  |
| `parentCommentId` | string |  |
| `post.id` | number |  |
| `post.name` | string |  |
| `post.slug` | string |  |
| `repliesCount` | number |  |
| `space.id` | number |  |
| `space.name` | string |  |
| `space.slug` | string |  |
| `url` | string |  |
| `user.avatarUrl` | string |  |
| `user.email` | string |  |
| `user.id` | number |  |
| `user.name` | string |  |
| `userCommentsCount` | number |  |
| `userLikesCount` | number |  |
| `userPostsCount` | number |  |

## Native endpoint

Through the native Circle API, this operation is `POST /api/admin/v2/comments` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

