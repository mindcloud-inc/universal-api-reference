# Front: Add Comment

Creates a conversation comment in Front.

```
POST https://connect.mindcloud.co/v1/universal/front/latest/actions/add-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/front/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "cnv_123",
  "body": "Internal note for this conversation."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/front/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "cnv_123",
    "body": "Internal note for this conversation."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | The conversation ID. Example: `cnv_123`. |
| `body` | string | yes | Content of the comment. Can include markdown formatting. Example: `Internal note for this conversation.`. |
| `isPinned` | boolean | no | Whether the comment is pinned in its conversation. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authorId` | string | no | ID of the teammate creating the comment. Example: `tea_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        "string"
      ],
      "author": {
        "customFields": {},
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "isAdmin": true,
        "isAvailable": true,
        "isBlocked": true,
        "lastName": "Chen",
        "links": {
          "related": {
            "conversations": "https://example.com",
            "inboxes": "https://example.com"
          },
          "self": "https://example.com"
        },
        "type": "string",
        "username": "Ava Chen"
      },
      "body": "string",
      "id": "string",
      "isPinned": true,
      "links": {
        "related": {
          "conversation": "https://example.com",
          "mentions": "https://example.com"
        },
        "self": "https://example.com"
      },
      "postedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array |  |
| `author.customFields` | object |  |
| `author.email` | string |  |
| `author.firstName` | string |  |
| `author.id` | string |  |
| `author.isAdmin` | boolean |  |
| `author.isAvailable` | boolean |  |
| `author.isBlocked` | boolean |  |
| `author.lastName` | string |  |
| `author.links.related.conversations` | string |  |
| `author.links.related.inboxes` | string |  |
| `author.links.self` | string |  |
| `author.type` | string |  |
| `author.username` | string |  |
| `body` | string |  |
| `id` | string |  |
| `isPinned` | boolean |  |
| `links.related.conversation` | string |  |
| `links.related.mentions` | string |  |
| `links.self` | string |  |
| `postedAt` | number |  |

## Native endpoint

Through the native Front API, this operation is `POST /conversations/:conversation_id/comments` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-comment.md) for the provider-specific parameters and requirements.

