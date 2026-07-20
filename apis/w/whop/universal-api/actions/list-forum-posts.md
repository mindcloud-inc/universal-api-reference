# Whop: List Forum Posts

Retrieves forum posts from the Whop platform.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-forum-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-forum-posts?connectionId=$CONNECTION_ID&experienceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experienceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-forum-posts?${params}`, {
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
| `experienceId` | string | yes | The unique identifier of the experience to list forum posts for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentCount": 1,
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isEdited": true,
      "isPinned": true,
      "isPosterAdmin": true,
      "likeCount": 1,
      "parentId": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {
        "id": "string",
        "name": "Ava Chen",
        "username": "Ava Chen"
      },
      "viewCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentCount` | number |  |
| `content` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `isEdited` | boolean |  |
| `isPinned` | boolean |  |
| `isPosterAdmin` | boolean |  |
| `likeCount` | number |  |
| `parentId` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `user` | object |  |
| `user.id` | string |  |
| `user.name` | string |  |
| `user.username` | string |  |
| `viewCount` | number |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/forum_posts` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forum-posts.md) for the provider-specific parameters and requirements.

