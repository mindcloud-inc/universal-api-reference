# Liveblocks: Add Comment Reaction

Creates a comment reaction in Liveblocks.

```
POST https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/add-comment-reaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/add-comment-reaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/add-comment-reaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commentId` | string | no | ID of the comment. |
| `roomId` | string | no | ID of the room. |
| `threadId` | string | no | ID of the thread. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "body": {},
      "createdAt": "string",
      "deletedAt": "string",
      "editedAt": "string",
      "id": "string",
      "metadata": {},
      "reactions": [
        {}
      ],
      "roomId": "string",
      "threadId": "string",
      "type": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `body` | object |  |
| `createdAt` | string |  |
| `deletedAt` | string |  |
| `editedAt` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `reactions` | array<object> |  |
| `roomId` | string |  |
| `threadId` | string |  |
| `type` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Liveblocks API, this operation is `POST /rooms/:roomId/threads/:threadId/comments/:commentId/add-reaction` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-comment-reaction.md) for the provider-specific parameters and requirements.

