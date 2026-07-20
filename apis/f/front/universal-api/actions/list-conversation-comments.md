# Front: List Conversation Comments

Retrieves a list of conversation comments from Front.

```
GET https://connect.mindcloud.co/v1/universal/front/latest/actions/list-conversation-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/list-conversation-comments?connectionId=$CONNECTION_ID&conversationId=cnv_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "cnv_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/list-conversation-comments?${params}`, {
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
| `conversationId` | string | yes | The conversation ID. Example: `cnv_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {
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
          "commentRepliedTo": {},
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
| `links.related.commentRepliedTo` | object |  |
| `links.related.conversation` | string |  |
| `links.related.mentions` | string |  |
| `links.self` | string |  |
| `postedAt` | number |  |

## Native endpoint

Through the native Front API, this operation is `GET /conversations/:conversation_id/comments` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversation-comments.md) for the provider-specific parameters and requirements.

