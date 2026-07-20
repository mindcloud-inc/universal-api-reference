# Circle: Get Basic Post

Retrieves basic post details from Circle by ID.

```
GET https://connect.mindcloud.co/v1/universal/circle/latest/actions/get-basic-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circle/latest/actions/get-basic-post?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circle/latest/actions/get-basic-post?${params}`, {
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
| `id` | number | yes | Post ID |

## Response

```json
{
  "success": true,
  "data": [
    {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body.body` | string |  |
| `body.createdAt` | date |  |
| `body.id` | number |  |
| `body.name` | string |  |
| `body.recordId` | number |  |
| `body.recordType` | string |  |
| `body.updatedAt` | date |  |
| `cardviewThumbnail` | string |  |
| `cardviewThumbnailUrl` | string |  |
| `commentsCount` | number |  |
| `communityId` | number |  |
| `coverImage` | string |  |
| `coverImageUrl` | string |  |
| `createdAt` | date |  |
| `customHtml` | string |  |
| `flaggedForApprovalAt` | string |  |
| `hideMetaInfo` | boolean |  |
| `id` | number |  |
| `isCommentsClosed` | boolean |  |
| `isCommentsEnabled` | boolean |  |
| `isLikingEnabled` | boolean |  |
| `likesCount` | number |  |
| `memberCommentsCount` | number |  |
| `memberLikesCount` | number |  |
| `memberPostsCount` | number |  |
| `name` | string |  |
| `publishedAt` | date |  |
| `slug` | string |  |
| `spaceId` | number |  |
| `spaceName` | string |  |
| `spaceSlug` | string |  |
| `status` | string |  |
| `tiptapBody` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `userAvatarUrl` | string |  |
| `userEmail` | string |  |
| `userId` | number |  |
| `userName` | string |  |

## Native endpoint

Through the native Circle API, this operation is `GET /api/admin/v2/posts/[:id]` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-basic-post.md) for the provider-specific parameters and requirements.

