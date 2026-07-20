# ContentStudio: Add Comment to Post

Adds a comment or internal note to a ContentStudio post.

```
POST https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/add-comment-to-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContentStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/add-comment-to-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "comment": "string",
  "post_id": "string",
  "workspace_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/add-comment-to-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "comment": "string",
    "post_id": "string",
    "workspace_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comment` | string | yes | Comment text. |
| `is_note` | boolean | no | True to save an internal note. |
| `mentioned_users[]` | array<string> | no | User IDs to mention. |
| `post_id` | string | yes | ContentStudio post ID. |
| `workspace_id` | string | yes | ContentStudio workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "isNote": true,
      "mentionedUsers": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `comment` | string |  |
| `createdAt` | date |  |
| `Id` | string |  |
| `isNote` | boolean |  |
| `mentionedUsers` | array<object> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native ContentStudio API, this operation is `POST /workspaces/:workspace_id/posts/:post_id/comments` (base URL `https://api.contentstudio.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-comment-to-post.md) for the provider-specific parameters and requirements.

