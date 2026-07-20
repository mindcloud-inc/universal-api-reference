# Front: List Conversation Followers

Retrieves a list of conversation followers from Front.

```
GET https://connect.mindcloud.co/v1/universal/front/latest/actions/list-conversation-followers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/list-conversation-followers?connectionId=$CONNECTION_ID&conversationId=cnv_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "cnv_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/list-conversation-followers?${params}`, {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `isAdmin` | boolean |  |
| `isAvailable` | boolean |  |
| `isBlocked` | boolean |  |
| `lastName` | string |  |
| `links.related.conversations` | string |  |
| `links.related.inboxes` | string |  |
| `links.self` | string |  |
| `type` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Front API, this operation is `GET /conversations/:conversation_id/followers` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversation-followers.md) for the provider-specific parameters and requirements.

