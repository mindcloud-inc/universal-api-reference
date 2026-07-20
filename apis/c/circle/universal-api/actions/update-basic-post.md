# Circle: Update Basic Post

Updates an existing basic post in Circle.

```
PUT https://connect.mindcloud.co/v1/universal/circle/latest/actions/update-basic-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/circle/latest/actions/update-basic-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circle/latest/actions/update-basic-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Post ID |
| `name` | string | no | Post name |
| `tiptapBody` | object | no | Tiptap body payload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "post": {
        "body": {
          "body": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "name": "Ava Chen",
          "recordId": 1,
          "recordType": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        },
        "cardviewThumbnail": "string",
        "cardviewThumbnailUrl": "https://example.com",
        "commentsCount": 1,
        "communityId": 1,
        "coverImage": "string",
        "coverImageUrl": "https://example.com",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "customHtml": "string",
        "flaggedForApprovalAt": "string",
        "hideMetaInfo": true,
        "id": 1,
        "isCommentsClosed": true,
        "isCommentsEnabled": true,
        "isLikingEnabled": true,
        "likesCount": 1,
        "memberCommentsCount": 1,
        "memberLikesCount": 1,
        "memberPostsCount": 1,
        "name": "Ava Chen",
        "publishedAt": "2026-05-07T12:00:00.000Z",
        "slug": "string",
        "spaceId": 1,
        "spaceName": "Ava Chen",
        "spaceSlug": "string",
        "status": "string",
        "tiptapBody": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com",
        "userAvatarUrl": "https://example.com",
        "userEmail": "ava@example.com",
        "userId": 1,
        "userName": "Ava Chen"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `post.body.body` | string |  |
| `post.body.createdAt` | date |  |
| `post.body.id` | number |  |
| `post.body.name` | string |  |
| `post.body.recordId` | number |  |
| `post.body.recordType` | string |  |
| `post.body.updatedAt` | date |  |
| `post.cardviewThumbnail` | string |  |
| `post.cardviewThumbnailUrl` | string |  |
| `post.commentsCount` | number |  |
| `post.communityId` | number |  |
| `post.coverImage` | string |  |
| `post.coverImageUrl` | string |  |
| `post.createdAt` | date |  |
| `post.customHtml` | string |  |
| `post.flaggedForApprovalAt` | string |  |
| `post.hideMetaInfo` | boolean |  |
| `post.id` | number |  |
| `post.isCommentsClosed` | boolean |  |
| `post.isCommentsEnabled` | boolean |  |
| `post.isLikingEnabled` | boolean |  |
| `post.likesCount` | number |  |
| `post.memberCommentsCount` | number |  |
| `post.memberLikesCount` | number |  |
| `post.memberPostsCount` | number |  |
| `post.name` | string |  |
| `post.publishedAt` | date |  |
| `post.slug` | string |  |
| `post.spaceId` | number |  |
| `post.spaceName` | string |  |
| `post.spaceSlug` | string |  |
| `post.status` | string |  |
| `post.tiptapBody` | string |  |
| `post.updatedAt` | date |  |
| `post.url` | string |  |
| `post.userAvatarUrl` | string |  |
| `post.userEmail` | string |  |
| `post.userId` | number |  |
| `post.userName` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Circle API, this operation is `PUT /api/admin/v2/posts/[:id]` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-basic-post.md) for the provider-specific parameters and requirements.

