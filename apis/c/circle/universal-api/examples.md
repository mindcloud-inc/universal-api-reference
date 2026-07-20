# Circle Universal API Examples

These examples use the MindCloud API key and Circle connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Basic Post

Retrieves basic post details from Circle by ID.

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

Example response:

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

See the full [Get Basic Post action reference](actions/get-basic-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/circle/latest/actions/get-basic-post).

## Add Space Member

Creates a new space membership in Circle.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circle/latest/actions/add-space-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "spaceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circle/latest/actions/add-space-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "spaceId": 1
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
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Space Member action reference](actions/add-space-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/circle/latest/actions/add-space-member).
